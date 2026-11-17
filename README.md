# League of Legends Characters Website

Site desenvolvido em **Angular** que apresenta personagens de League of Legends.
Projeto criado para praticar desenvolvimento com framework front-end e entrega contínua (CI/CD) com **GitHub Actions** e **Coolify**.

## Tecnologias

- **Angular** (TypeScript, HTML e CSS)
- **Docker**: o `Dockerfile` gera a imagem da aplicação, servida na porta 80
- **GitHub Actions**: integração contínua (build e validação da imagem a cada push)
- **Coolify**: plataforma de deploy que publica a aplicação a partir deste repositório

## Estrutura do projeto

```
├── .github/workflows/deploy.yml   # Pipeline de CI/CD
├── src/                           # Código-fonte da aplicação Angular
├── Dockerfile                     # Build da imagem usada no deploy
├── docker-compose.yml             # Execução local com Docker
├── angular.json                   # Configuração do Angular
└── package.json                   # Dependências e scripts
```

## Como rodar localmente

### Com Node.js

```bash
npm install
npm start
```

Acesse `http://localhost:4200`.

### Com Docker

```bash
docker compose up --build
```

Acesse `http://localhost:8080`.

## CI/CD

A cada push na branch `main`:

1. O **GitHub Actions** instala as dependências, faz o build do Angular e valida a imagem Docker.
2. Se tudo passar, o workflow aciona o **Coolify**, que constrói a imagem a partir do `Dockerfile` e publica a nova versão.

## Aplicação publicada

http://ffiktk6q7ki2ulzivdf6o6ie.187.33.201.107.sslip.io

## Autora

Vi Nogueira de Souza · 3º ADS · FEMA
