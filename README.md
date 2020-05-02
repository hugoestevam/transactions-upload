# Transactions - Upload

Para executar este projeto em seu potencial é necessário ter o Node rodando na máquina.

#### Dependencias
Todas as dependencias podem ser opcionalmente instaladas através do [Chocolatey](https://chocolatey.org/).

##### NodeJS
* Obtenha o NodeJS pelo:
 * [Site oficial](https://nodejs.org/), ou use
 
        > choco install nodejs
 
##### Git
* Obtenha o git pelo:
 * [Site oficial](https://git-for-windows.github.io/), ou use:

        > choco install git
 
#### Baixando o Projeto

O download do projeto pode ser feito através do `git` seguindo os passos:

    -aponte para a pasta da solução
     > git clone https://github.com/hugoestevam/transactions-upload.git

#### Preparando o ambiente

##### Resumo dos comandos
    
-Você pode instalar o yarn globalmente através do seguinte comando:    

    > choco install yarn
        
-Na pasta do projeto, rode esse comando para executar a instalação dos pacotes:

    > yarn install         
        
-Execute esse comanco para subir o servidor Node.

    > yarn dev:server

-Para executar os testes através do Jest, basta rodar o comando abaixo:

    > yarn test


##### Detalhes

* Se estiver usando Windows, inicie o prompt com permissões de administrador para que **choco install** funcione corretamente.
* Ao rodar o comando **yarn dev:server** o ts-node-dev vai executar um servidor com a função HotReload ativada.
* Se tudo estiver ok, o prompt irá listar todas as saídas abaixo.

```shell
❯ yarn dev:server
yarn run v1.22.0
$ ts-node-dev --inspect=9230 --transpileOnly --ignore-watch node_modules src/server.ts
Ignore watch: [ 'node_modules' ]
Using ts-node version 8.8.2, typescript version 3.8.3
Debugger listening on ws://127.0.0.1:9230/3898c6e4-1365-42d7-af13-99e7e8ef2662
For help, see: https://nodejs.org/en/docs/inspector
🚀 Server started on port 3333!
```
#### Executando
Basicamente deve estar executando a API Node. A aplicação já deve estar executando em  [http://localhost:3333](http://localhost:3333). 

* [Jest](https://jestjs.io/)
    * Você pode executar os testes através do comando `> yarn test`;

```shell
❯ yarn test 
yarn run v1.22.0
$ cross-env NODE_ENV=test jest
 PASS  src/__tests__/Transaction.spec.ts
  Transaction
    ✔ should be able to list transactions (182ms)
    ✔ should be able to create new transaction (56ms)
    ✔ should create tags when inserting new transactions (55ms)
    ✔ should not create tags when they already exists (48ms)
    ✔ should not be able to create outcome transaction without a valid balance (47ms)
    ✔ should be able to delete a transaction (70ms)
    ✔ should be able to import transactions (61ms)

Test Suites: 1 passed, 1 total
Tests:       7 passed, 7 total
Snapshots:   0 total
Time:        2.292s, estimated 3s
Ran all test suites.
Done in 3.28s.
```

## FIM

Qualquer dúvida entre em contato comigo!
Obrigado.