### 🏬 Sistema de Gerenciamento de Estoque (SGE)

Um sistema completo para controle de estoque, gestão de produtos e movimentações, desenvolvido com Django, Django REST Framework e Bootstrap

## 🎨 Demonstração  

### 📌 Página principal - Dashboard
<div align="center">
  <img src="https://github.com/user-attachments/assets/a3f1cbd1-7eee-4d4b-b5b7-e992db69fe71" alt="Lista de carros" width="800">
</div>


## 🚀 Tecnologias Utilizadas
- **Backend:** Django, Django REST Framework 
- **Frontend:** Django Templates, Bootstrap 5
- **Banco de Dados:** SQLite (pode ser substituído por outro banco relacional)
- **Autenticação:** JWT com `rest_framework_simplejwt`
- **Outras Ferramentas:** Flake8 para boas práticas

## 📂 Estrutura do Projeto  
A aplicação é modularizada com diferentes apps:
-**brands:** Gerencia as marca
- **categories:** Gerencia categorias de produtos  
- **inflows:** Registra entradas no estoque  
- **outflows:** Registra saídas do estoque  
- **products:** Gerencia produtos no sistema  
- **suppliers:** Cadastro e gestão de fornecedores  

## 🎨 Interface  
A interface do sistema foi construída utilizando **Django Templates** com **Bootstrap 5**, garantindo um design responsivo e amigável para o usuário.  

## 🔑 Autenticação  
O sistema utiliza **JWT (JSON Web Token)** para autenticação segura das APIs.  
- Para obter um token de acesso:  
  ```bash
  POST /api/token/  
  { "username": "seu_usuario", "password": "sua_senha" }
  ```  
- Para renovar o token:  
  ```bash
  POST /api/token/refresh/  
  { "refresh": "seu_refresh_token" }
  ```  

## ⚙️ Configuração do Ambiente  
1. Clone o repositório:  
   ```bash
   git clone https://github.com/ldickmann/djangoSGE.git
   cd djangoSGE
   ```  
2. Crie um ambiente virtual e instale as dependências:  
   ```bash
   python -m venv venv
   source venv/bin/activate  # No Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```  
3. Execute as migrações:  
   ```bash
   python manage.py migrate
   ```  
4. Crie um superusuário para acessar o painel admin:  
   ```bash
   python manage.py createsuperuser
   ```  
5. Inicie o servidor:  
   ```bash
   python manage.py runserver
   ```  

## 🔗 Endpoints e Rotas
- **Admin:** `/admin/`
- **Páginas Frontend:**
  - Página inicial: `/`
  - Lista de produtos: `/products/`
  - Entrada de estoque: `/inflows/`
  - Saída de estoque: `/outflows/`
- **APIs:**
  - Produtos: `/api/products/`
  - Movimentações: `/api/inflows/` e `/api/outflows/`
  - Autenticação JWT: `/api/token/` e `/api/token/refresh/`

## Desenvolvedor
Desenvolvido por **Lucas Elias Dickmann** ao decorror do curso Django Master - Aplicações Web com Python e Django da PycodeBR Treinamentos.

-
-

Sistema em constante evolução!

---

Se quiser adicionar mais detalhes sobre a API, modelos ou incluir prints da interface, me avise!
