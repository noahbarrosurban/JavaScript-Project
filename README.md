# JavaScript-Project

> “A verdadeira viagem de descoberta não consiste em procurar novas paisagens, mas em ter novos olhos.” — Marcel Proust

![node](https://badgen.net/badge/Node.js/14+/green?scale=1.2) ![express](https://badgen.net/badge/Express/4.x/blue?scale=1.2) ![sequelize](https://badgen.net/badge/Sequelize/6.x/purple?scale=1.2) ![mssql](https://badgen.net/badge/MS%20SQL%20Server/2022/red?scale=1.2) ![react](https://badgen.net/badge/React/17+/cyan?scale=1.2) ![bootstrap](https://badgen.net/badge/Bootstrap/5.x/violet?scale=1.2)

**Olá, Dev!**

Este projeto é uma aplicação full stack usando Node.js, Express, Sequelize, MS SQL Server no backend, e React e Bootstrap no frontend. Este guia fornece as instruções para configurar e rodar o projeto localmente.

## Pré-requisitos

Para continuar, atente aos pré-requisitos:

- Node.js
    - Como instalar?
        - Instalação manual: [Baixar](https://nodejs.org/en/download/) (versão 14.0 ou superior)
- npm        
    - Como instalar?
        - Instalação manual: [Baixar](https://www.npmjs.com/get-npm) (geralmente instalado junto com o Node.js)
- Docker
    - Como instalar?
        - Instalação manual: [Baixar](https://www.docker.com/get-started)

## Configuração do Backend

1. **Inicie o contêiner Docker para o MS SQL Server:**

   Execute o seguinte comando no terminal para iniciar um contêiner Docker com o MS SQL Server:

   ```bash
   docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=YourStrongPassw0rd' -p 1433:1433 --name mssql -d mcr.microsoft.com/mssql/server
   ```

2. **Instale a CLI do MS SQL Server:**

   Para gerenciar o banco de dados, instale a CLI do MS SQL Server:

   ```bash
   npm install -g sql-cli
   ```

3. **Conecte-se ao banco de dados e crie a base de dados `React`:**

   Conecte-se ao banco de dados usando a CLI e crie a base de dados `React`:

   ```bash
   mssql -u sa -p YourStrongPassw0rd -s localhost -o 1433
   ```

   Depois de conectado, execute:

   ```sql
   CREATE DATABASE React;
   ```

4. **Abra um novo terminal e navegue até o diretório `backend`:**

   ```bash
   cd backend
   ```

5. **Instale as dependências do backend:**

   ```bash
   npm install
   ```

6. **Inicie o servidor backend:**

   ```bash
   npm start
   ```

   Você deve ver a mensagem `Server listening on port 8081`.

## Configuração do Frontend

1. **Abra um novo terminal e navegue até o diretório `frontend`:**

   ```bash
   cd frontend
   ```

2. **Instale as dependências do frontend:**

   ```bash
   npm install axios bootstrap
   ```

3. **Inicie o servidor frontend:**

   ```bash
   npm start
   ```

   Você deve ver a aplicação rodando em [localhost:3000](`http://localhost:3000`).


## Onde obter ajuda?

Para sanar quaisquer dúvidas, procure o Engenheiro de Software responsável pelo projeto.