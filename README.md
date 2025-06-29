# Seletivo AwSales

Este repositório contém o projeto do teste técnico para processo seletivo da empresa AWSales. Abaixo estão as instruções para configurar e rodar o projeto localmente utilizando Docker.

## Tecnologias
 Frontend:
- Next.js | Typescript
- Docker + Docker Compose
- Deploy - Vercel

 Backend:
- Node.js / TypeScript 
- Jest
- PostgreSQL + Sequelize
- Docker + Docker Compose
- Deploy - AWS

## Pré-requisitos

Antes de começar, você precisa ter instalado na sua máquina:

- Git: https://git-scm.com/
- Docker e Docker compose: https://www.docker.com/
- Acesso ao terminal / prompt de comando

## Como rodar o projeto

### 1. Clonar o repositório com os submódulos

```bash
git clone --recurse-submodules https://github.com/jordan-cod/seletivo-mamba.git
cd seletivo-mamba
```

Se esquecer a flag, use:

```bash
git submodule update --init --recursive
```

---

### 2. Configurar as variáveis de ambiente

Crie um arquivo `.env` na raiz do projeto com base no `.env.example`:

```sh
cp .env.example .env
```

Preencha os valores necessários de acordo com sua configuração local.

⚠️ Importante: Verifique se as portas configuradas no `.env` não estão sendo usadas por outros serviços.

### 3. Rodar os containers com Docker

```bash
docker-compose up --build -d
```

---

### 4. Testar os serviços

Acesse via navegador:

- 🟢 Frontend: http://localhost:{FRONTEND_PORT}
- 🟢 Backend: http://localhost:{BACKEND_PORT}/docs

---

## 📁 Estrutura do repo

```
seletivo-mamba/
├── modules/
│   ├── backend/     # Submódulo Git
│   ├── frontend/    # Submódulo Git
├── docker-compose.yml
├── .env.example
├── .env             # Arquivo de variáveis de ambiente
├── .gitignore
├── .gitmodules
└── README.md
```

---

A documentação de cada serviço está disponível em seu próprio repositório Git.
Cada projeto pode ser rodado individualmente clonando o repositório e seguindo as instruções de cada projeto.
