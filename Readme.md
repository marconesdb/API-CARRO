### README.md

```markdown
# Projeto CRUD

Este é um projeto Node.js que utiliza Express e MySQL para criar uma API CRUD de gerenciamento de carros.

## Instalação

Para rodar este projeto localmente, siga os passos abaixo:

### 1. Clone o repositório

```bash
git clone https://github.com/marconesdb/API-CARRO.git

``` 
Navegue até a pasta API-CARROS com o comando:

```bash
cd API-CARRO
```
### 2. Instale as dependências

Para instalar todas as dependências do projeto, você precisa ter o Node.js instalado. No terminal, execute:

```bash
npm init -y
```

Depois: 

```bash
npm install express mysql dotenv cors body-parser
```

Isso instalará todas as dependências listadas no arquivo `package.json`, incluindo `express`, `mysql`, `dotenv`, `cors`, `body-parser`.

### 3. Instale o nodemon (dependência de desenvolvimento)

`nodemon` é uma ferramenta que ajuda a desenvolver aplicativos baseados em Node.js reiniciando automaticamente a aplicação quando arquivos são modificados. Para instalar o `nodemon`, execute:

```bash
npm install nodemon --save-dev
```

No arquivo `package.json`, em `scripts`, adicione ou verifique se já está com a linha de código abaixo para que o `nodemon` localize o arquivo `server.js` e inicie o servidor com o comando `npm start`:

```json
"start": "nodemon ./src/server.js"
```

## Configuração

Antes de iniciar o servidor, é necessário configurar as variáveis de ambiente. Crie um arquivo `.env` na raiz do projeto e configure as variáveis conforme necessário. Por exemplo:

```
DB_HOST=localhost
DB_USER=seu_usuario
DB_PASSWORD=sua_senha
DB_DATABASE=nome_do_banco_de_dados
```

 Essas variáveis são utilizadas para configurar a conexão com o banco de dados MySQL.

## Criando o Banco de Dados

Crie o banco de dados com o comando:

```sql
CREATE DATABASE nome_do_banco_de_dados;
```

## Crie a tabela do Banco de Dados:

```sql
USE nome_do_banco_de_dados;

CREATE TABLE nome_da_tabela (
    codigo INT PRIMARY KEY AUTO_INCREMENT,
    modelo VARCHAR(30),
    placa VARCHAR(7)
);
```

## Preencha seu Banco de Dados com cadastros, Ex:

```sql
INSERT INTO nome_da_tabela (modelo, placa) VALUES ('Toyota Corolla', 'HDP9645');
INSERT INTO nome_da_tabela (modelo, placa) VALUES ('Fiat Cronos', 'HDP9645');
```
## Veja a tabela do Banco de Dados preenchida com o comando:

```bash

SELECT * FROM nome_da_tabela;

```
  
## Executando o Projeto

Após a instalação das dependências e configuração das variáveis de ambiente, você pode iniciar o servidor localmente. Execute:

```bash
npm start
```

Isso iniciará o servidor Node.js utilizando `nodemon`, que reiniciará automaticamente a aplicação sempre que houver mudanças nos arquivos.

Você verá no console do terminal a mensagem: 

Servidor rodando em: http://localhost:3000
Conectado ao Banco de Dados: nome_do_seu_banco_de_dados

## Testando as Rotas

- **GET**: `http://localhost:3000/api/carros`  
  Lista todos os carros cadastrados.

- **GET**: `http://localhost:3000/api/carro/1`  
  Lista o carro cadastrado com código ID-1.

- **POST**: `http://localhost:3000/api/carro`  
  Envia um novo cadastro de carro no banco de dados.

- **PUT**: `http://localhost:3000/api/carro/1`  
  Faz uma alteração no cadastro de carro de código ID-1 no banco de dados.

- **DELETE**: `http://localhost:3000/api/carro/1`  
  Deleta um cadastro de carro com o ID-1 no banco de dados.

## Estrutura do Projeto

- `src/`: Pasta que contém os arquivos-fonte da aplicação.
- `src/server.js`: Arquivo principal que configura e inicia o servidor Express.
- `src/routes.js`: Arquivo que define as rotas da API.
- `src/controllers/`: Pasta que contém os controladores da aplicação.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para enviar pull requests para melhorias no código, documentação, ou reportar problemas abrindo uma issue.

```

### Explicação do README.md

- **Descrição**: Descreve brevemente o projeto.
- **Instalação**: Instruções para clonar o repositório e instalar as dependências necessárias com `npm install`.
- **Configuração**: Instruções para configurar as variáveis de ambiente no arquivo `.env`.
- **Executando o Projeto**: Como iniciar o servidor localmente com `npm start`.
- **Estrutura do Projeto**: Explica a estrutura básica de pastas e arquivos do projeto.
- **Contribuição**: Incentiva contribuições para o projeto.

Este `README.md` fornece uma orientação clara e concisa para quem deseja configurar e executar o seu projeto Node.js. Certifique-se de personalizar conforme necessário para o seu projeto específico.