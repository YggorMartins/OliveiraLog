# 🚚 OliveiraLog API

> API REST para gerenciamento de entregas e encomendas, desenvolvida com Node.js, TypeScript, Express e Prisma.

O **OliveiraLog** é uma API backend criada para simular operações de logística e entrega de encomendas.

O projeto permite gerenciar usuários, autenticação, entregas e histórico de movimentações, utilizando **JWT para autenticação** e **RBAC (Role-Based Access Control)** para controle de permissões.

---

## 🎯 Objetivo do projeto

O projeto foi desenvolvido com foco em praticar e demonstrar conceitos importantes de desenvolvimento backend, como:

- Construção de APIs REST
- Autenticação com JWT
- Autorização baseada em papéis (RBAC)
- Validação de dados
- Persistência de dados com PostgreSQL
- ORM com Prisma
- Organização de responsabilidades no backend
- Testes automatizados
- Containerização do banco de dados

---

## ✨ Funcionalidades

### 👤 Usuários

- Cadastro de usuários
- Autenticação
- Controle de acesso por função
- Diferentes níveis de acesso

Funções disponíveis atualmente:

- `customer`
- `sale`

### 📦 Entregas

- Criação de entregas
- Listagem de entregas
- Atualização do status das entregas
- Controle do ciclo de entrega

### 📝 Histórico de entregas

Cada alteração de status pode gerar um registro no histórico da entrega, permitindo acompanhar as movimentações da encomenda.

### 🔐 Segurança

- Autenticação utilizando JWT
- Senhas protegidas
- Middleware de autenticação
- Controle de acesso baseado em roles (RBAC)

---

## 🛠️ Tecnologias

### Backend

![Node.js](https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Express](https://img.shields.io/badge/Express-4.x-000000?style=for-the-badge&logo=express&logoColor=white)

### Database

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-ORM-2D3748?style=for-the-badge&logo=prisma&logoColor=white)

### Segurança e validação

![JWT](https://img.shields.io/badge/JWT-Authentication-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-Validation-3E67B1?style=for-the-badge)

### Testes e infraestrutura

![Jest](https://img.shields.io/badge/Jest-Testing-C21325?style=for-the-badge&logo=jest&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

---

## 🏗️ Estrutura do projeto

O projeto está organizado em módulos para separar responsabilidades entre rotas, controllers, middlewares, banco de dados e testes.

```text
OliveiraLog/
├── prisma/
├── src/
│   ├── configs/
│   ├── controllers/
│   ├── database/
│   ├── middlewares/
│   ├── routes/
│   ├── tests/
│   ├── types/
│   ├── utils/
│   ├── app.ts
│   ├── env.ts
│   └── server.ts
│
├── .env-example
├── docker-compose.yml
├── jest.config.ts
├── package.json
├── tsconfig.json
└── README.md
```

🔄 Arquitetura da aplicação 
```
Cliente
   │
   ▼
Routes
   │
   ▼
Middleware
   │
   ▼
Controllers
   │
   ▼
Prisma ORM
   │
   ▼
PostgreSQL
```

A aplicação utiliza uma separação de responsabilidades entre rotas, middlewares, controllers e persistência de dados.

🔐 Autenticação e autorização

A autenticação da aplicação utiliza JSON Web Token (JWT).

Após realizar o login, o usuário recebe um token que deve ser utilizado nas requisições protegidas.

O projeto também utiliza RBAC (Role-Based Access Control) para limitar determinadas operações de acordo com o papel do usuário.

Exemplo:

Usuário
   │
   ├── customer
   │
   └── sale

As senhas são protegidas utilizando bcrypt.

🧩 Principais módulos
Sessions

Responsável pelo processo de autenticação dos usuários.

Users

Responsável pelo cadastro e gerenciamento dos usuários.

Deliveries

Responsável pelo gerenciamento das encomendas e seus status.

Delivery Logs

Responsável pelo histórico das movimentações das entregas.

🌐 Rotas principais

A API possui módulos de rotas separados para:

Sessions
Users
Deliveries
Delivery Logs

As implementações estão organizadas dentro de src/routes.

✅ Testes

O projeto utiliza Jest e Supertest para testes automatizados.

Existem testes relacionados aos módulos de:

Autenticação
Usuários

Estrutura:

src/
└── tests/
    ├── sessions-controller.test.ts
    └── user-controller.test.ts

Para executar os testes:

npm run test:dev
🐳 Docker

O PostgreSQL pode ser executado utilizando Docker Compose.

Subir o banco
docker compose up -d

Banco configurado para ambiente local:

Host: localhost
Port: 5432
Database: oliveiraLog
User: postgres
Password: postgres

Em ambientes reais, utilize credenciais seguras e variáveis de ambiente.

⚙️ Como executar
1. Clone o repositório
git clone https://github.com/YggorMartins/OliveiraLog.git
2. Entre no diretório
cd OliveiraLog
3. Instale as dependências
npm install
4. Configure o ambiente

Crie um arquivo .env baseado no .env-example.

5. Suba o PostgreSQL
docker compose up -d
6. Execute as migrations
npx prisma migrate dev
7. Inicie a aplicação
npm run dev
🧪 Executando os testes
npm run test:dev
📦 Build

Para gerar a versão compilada:

npm run build

Para executar a versão compilada:

npm start

📚 O que este projeto demonstra

Este projeto demonstra conhecimentos práticos em:

Node.js
TypeScript
Express
APIs REST
Prisma ORM
PostgreSQL
JWT
RBAC
Zod
Jest
Supertest
Docker
Git e GitHub
Organização de código backend


👨‍💻 Autor

Yggor Martins

Java Backend / Fullstack Developer

🔗 GitHub

🔗 LinkedIn

🌐 Portfólio

⭐ Se você gostou do projeto, considere deixar uma estrela no repositório.
