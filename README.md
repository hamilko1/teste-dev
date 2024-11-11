# Projeto Rick and Morty API - Teste de Desenvolvimento
## Tecnologias Utilizadas

- **Backend:**
  - [Laravel](https://laravel.com/) (PHP) para o gerenciamento da API e lógica de backend.
  - [Node.js](https://nodejs.org/) para rodar o servidor e interagir com o frontend.
  
- **Frontend:**
  - [React](https://reactjs.org/) para construção da interface de usuário.
  - **Axios** para fazer requisições HTTP ao backend e à API externa.

- **Outras Dependências:**
  - [Composer](https://getcomposer.org/) para gerenciar dependências PHP.
  - [NPM](https://www.npmjs.com/) para gerenciar dependências JavaScript.

## Pré-requisitos

Antes de rodar o projeto localmente, o avaliador precisa garantir que as seguintes ferramentas estejam instaladas em seu computador:

- **Git**: Para clonar o repositório.
- **PHP (versão 7.x ou superior)**: Requerido para o Laravel.
- **Composer**: Para instalar dependências PHP do Laravel.
- **Node.js e NPM**: Para rodar o React e o servidor de desenvolvimento.
- **MySQL ou MariaDB**: Para o banco de dados (dependendo do que você usou no projeto).

## Passos para Configuração

### 1. Clonar o Repositório

Primeiro, clone o repositório do projeto em seu diretório local com o seguinte comando:
```bash
git clone https://github.com/seuusuario/rick-morty-api.git
```

Entre no diretório do projeto:
```bash
cd rick-morty-api
```

### 2. Configuração do Backend (Laravel)
2.1 Instalar Dependências do Laravel

  No terminal, dentro da pasta do projeto, execute o comando para instalar as dependências PHP do Laravel:
  ```bash  
  composer install
  ```

2.2 Configurar o Banco de Dados

  Crie um banco de dados MySQL ou MariaDB. Se você não tiver um banco de dados específico, pode criar um com o nome rick_morty_db:
   ```sql
  CREATE DATABASE rick_morty_db;
  ```
  No diretório do projeto, copie o arquivo .env.example para .env:
  ```bash 
  cp .env.example .env
  ```
  Abra o arquivo .env e configure os detalhes do banco de dados:
 ```sql
  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=rick_morty_db
  DB_USERNAME=root
  DB_PASSWORD=
  ```
  Execute a migração para criar as tabelas necessárias no banco de dados:
  ```bash
  php artisan migrate
  ```
2.3 Rodar o Backend

Agora, você pode iniciar o servidor backend do Laravel. No terminal, execute o seguinte comando:
  ```bash  
  php artisan serve
   ```
O Laravel estará rodando localmente em http://localhost:8000.

### 3. Configuração do Frontend (React)
3.1 Instalar Dependências do React

  Navegue até o diretório do frontend, onde o React está localizado. Se o projeto estiver em uma pasta separada, entre nela:
  ```bash  
  cd frontend
  ```
  Instale as dependências do React com o seguinte comando:
  ```bash 
  npm install
  ```
3.2 Rodar o Frontend

Agora, para rodar a aplicação React em um ambiente local, execute:
  ```bash 
  npm start
  ```
Isso abrirá a aplicação React no navegador em http://localhost:3000.

4. Testar o Projeto

Após configurar e rodar tanto o backend quanto o frontend, você pode testar a aplicação acessando as rotas e interagindo com a interface. A aplicação deve consumir dados da API do Rick and Morty e exibir as informações de personagens, episódios e locais.

  Na interface do React, você verá as informações listadas, e será capaz de pesquisar e interagir com os dados da API.
  As requisições feitas no frontend serão enviadas ao backend Laravel, que então consulta a API externa e retorna os dados para o frontend.

5. Funcionalidades a Testar

    Exibição de Personagens: A aplicação deve exibir uma lista de personagens de Rick and Morty.
    Busca de Personagens: O usuário deve ser capaz de pesquisar por personagens.
    Exibição de Episódios: A aplicação também deve mostrar informações sobre episódios, com base nos dados da API.
    Exibição de Locais: Dados sobre os locais também devem ser mostrados na interface.

6. Considerações Finais

Este projeto integra Laravel para gerenciar a parte de backend, Node.js como servidor de desenvolvimento e React para renderizar a interface. Ele foi feito para consumir e exibir dados da API do Rick and Morty.
