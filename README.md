# 🚚 OliveiraLog API

API de gerenciamento de logística e entregas desenvolvida com Node.js, Express e Prisma. O projeto foca em controle de encomendas, autenticação JWT e permissões de acesso (RBAC).

---

## Português

### ✨ Funcionalidades
- **Gestão de Usuários**: Cadastro e login com diferentes níveis de acesso (`customer`, `sale`).
- **Controle de Entregas**: Criação, listagem e atualização de status de encomendas.
- **Logs de Entrega**: Registro automático de cada movimentação ou alteração de status.
- **Segurança**: Autenticação via JWT e controle de rotas por papel (Role).

### 🛠️ Tecnologias
- **Node.js & TypeScript**
- **Prisma ORM** (PostgreSQL)
- **Docker** (Banco de dados)
- **Zod** (Validação de dados)
- **Jest** (Testes)
- **Insomnia** (Testes de requisição)

### 🚀 Como executar
1. Clone o repositório.
2. Configure o `.env` baseado no `.env-example`.
3. Suba o banco: `docker-compose up -d`.
4. Instale as dependências: `npm install`.
5. Rode as migrations: `npx prisma migrate dev`.
6. Inicie o servidor: `npm run dev`.

---

## English

### ✨ Features
- **User Management**: Registration and login with access levels (`customer`, `sale`).
- **Delivery Control**: Create, list, and update delivery status.
- **Delivery Logs**: Automatic tracking of every package movement.
- **Security**: JWT authentication and Role-Based Access Control (RBAC).

### 🛠️ Tech Stack
- **Node.js & TypeScript**
- **Prisma ORM** (PostgreSQL)
- **Docker** (Database)
- **Zod** (Validation)
- **Jest** (Testing)
- **Insomnia** (API testing)

### 🚀 Getting Started
1. Clone the repository.
2. Set up your `.env` (check `.env-example`).
3. Start the database: `docker-compose up -d`.
4. Install dependencies: `npm install`.
5. Run migrations: `npx prisma migrate dev`.
6. Start the server: `npm run dev`.

---

**Desenvolvido por Yggor Martins** 🚀
