# json-server-base

Esse é o repositório com a base de JSON-Server + JSON-Server-Auth já configurada, feita para ser usada no desenvolvimento das API's nos Capstones do Q2.

## Endpoints

Assim como a documentação do JSON-Server-Auth traz (https://www.npmjs.com/package/json-server-auth), existem 3 endpoints que podem ser utilizados para cadastro e 2 endpoints que podem ser usados para login.

### Cadastro

POST /register <br/>
POST /signup <br/>
POST /users

Qualquer um desses 3 endpoints irá cadastrar o usuário na lista de "Users", sendo que os campos obrigatórios são os de email e password.
Você pode ficar a vontade para adicionar qualquer outra propriedade no corpo do cadastro dos usuários.


### Login

POST /login <br/>
POST /signin

Qualquer um desses 2 endpoints pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

### Posts
rota privada - precisa de autenticação com o token

POST/posts <br/>

esse endpoint pode ser usado por um usuario logado para ele fazer um post que publico, onde qualquer pessoa pode ver, mas somente o proprio usuario pode modificar o post.

o corpo da requisição deve ser no seguinte formato:
{
    "title": "titulo para o post",
    "content": "conteudo do post",
    "userId": id do usuario
}

rota publica 

GET/posts <br/>

esse endpoint pode ser usado para listar todos os posts publicos que qualquer usuario pode ver.


### Posts Privados
rota privada - precisa de autenticação com o token

POST/privatePosts <br/>

esse endpoint pode ser usada um usuario logado para ele fazer um post que privado, onde somente outros usuarios logados podem ver e somente o proprio dono pode modificar o post.

rota privada - precisa de autenticação com o token

GET/privatePosts <br/>

esse endpoint pode ser usado para listar todos os posts privados que qualquer usuario logado pode ver.



