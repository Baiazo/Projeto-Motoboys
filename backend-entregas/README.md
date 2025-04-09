# 📦 Backend do Sistema de Entregas (Agência & Motoboys)

Este é o backend de um sistema de gerenciamento de entregadores via agências (chefe dos motoboys). A aplicação foi desenvolvida em **Node.js + Express + PostgreSQL**, com autenticação JWT e organização por camadas (controllers, routes, middleware, etc).

---

## ✅ Requisitos

Antes de começar, você precisará ter instalado:

- [Git](https://git-scm.com/)
- Node.js e npm
- PostgreSQL

### 🔧 Instalando no Ubuntu 22.04/24.04

#### Instalar Node.js + npm
```bash
sudo apt update
sudo apt install nodejs npm -y
```

> (Opcional, mas recomendado): Instalar com NVM (Node Version Manager)
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
source ~/.bashrc
nvm install --lts
```

#### Instalar PostgreSQL
```bash
sudo apt install postgresql postgresql-contrib -y
```

#### Verificar se está tudo instalado:
```bash
node -v
npm -v
psql --version
```

---

## 🚀 Instalação e Execução do Projeto

1. **Clone o projeto**
```bash
git clone https://github.com/Baiazo/Projeto-Motoboys.git
cd backend-entregas
```

2. **Instale as dependências**
```bash
npm install
```

3. **Configure o banco de dados**

Abra o PostgreSQL e crie o banco:
```bash
sudo -u postgres psql
CREATE DATABASE entregas_app;
\q
```

4. **Crie um arquivo `.env` com os seguintes dados:**
```env
PORT=3000
DB_HOST=localhost
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=sua_senha
DB_DATABASE=entregas_app
JWT_SECRET=umasecretachaveaqui
```

5. **Inicie o servidor**
```bash
npm run dev
```

A API estará disponível em `http://localhost:3000`

---

## 📂 Estrutura de Diretórios

```
backend-entregas/
├── controllers/
├── routes/
├── models/
├── middleware/
├── config/
├── .env
├── index.js
├── package.json
└── README.md
```

---

## 📮 Rotas Iniciais (Exemplo)

- `POST /usuarios` → Cadastro de usuário
- `POST /auth/login` → Login e geração de token
- `GET /entregadores` → Listagem (rota protegida)

---

## 📄 Licença

Este projeto é open-source, sinta-se à vontade para contribuir.
