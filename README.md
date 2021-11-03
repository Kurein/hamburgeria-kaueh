# hamburgeria-kaueh

Esse é o repositório com uma base de uma API de Hamburgeria, onde existem variados lanches e produtos que podem ser colocados em um carrinho do usuário



Link da API: https://hamburgeria-kaueh.herokuapp.com/

## Endpoints

A API conta com um total de 7 Endpoits sendo eles relacionados com: listagem de usuários, registrar, logar, lista de produtos, acesso ao carrinho do usuário, assim como endpoits para manuseio do carrinho, como adicionar, modificar, e retirar itens do carrinho 

<h2 align ='center'> Cadastro e Login </h2>

### Cadastro

Um Endpoint básico de cadastro de usuário

POST /register <br/>

body:

{ <br/>
"email":<br/>
"password":<br/>
"name":<br/>
}<br/>

### Login

Um outro Endpoint básico para logar o usuário

POST /login <br/>

body:

{<br/>
"email":<br/>
"password":<br/>
}<br/>

<h2 align ='center'> Endpoints que não precisam de uma autenticação </h2>

### Lista de Usuários

GET /users <br/>

E para ter acesso a um usuário em específico

GET /users/id <br/>

### Lista de Produtos

GET /products <br/>

<h2 align ='center'> Endpoints que precisam de uma autenticação </h2>

### Acesso ao Carrinho

GET /cart

Para ter acesso a um item em específico do carrinho

GET /cart/itemId <br/>

### Adicionar item ao carrinho

POST /cart <br/>

body:

{<br/>
"name":<br/>
"category":<br/>
"price":<br/>
"img": <br/>
"userId":<br/>
}<br/>

### Modificar item no carrinho

PATCH /cart/itemId <br/>

### Retirar item do carrinho

DELETE /cart/itemId
