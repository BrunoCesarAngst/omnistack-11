# Ajuda

```js
/**
 * Métodos HTTP:
 * GET: Buscar/listar uma informação no back-end
 * POST: Criar uma informação no back-end
 * PUT: Alterar uma informação no back-end
 * DELETE: Deletar uma informação no back-end
 * 
 * Rotas 
 * app.get('/users')
 * app.método(get)('rota(/) recurso(users)
 * recurso(users) qual é a entidade a tabela no banco que estou buscado os dados
 * 
 * Tipos de parâmetros
 * Query Params: Parâmetros nomeados enviados na rota na url após "?" para
 * paginar, filtrar
 * ex. http://localhost:3333/users?page=2&name=Bruno&idade=37
 * 
 * Route Params: Parâmetros para identificar recursos
 * app.get('/users/:id', (req, res) => {
 * buscando os dados de um único usuário sempre recebendo os parâmetros
 * esperados nuca a mais
 * ex. http://localhost:3333/users/1
 * 
 * Request Body: É o corpo da requisição, utilizado para criar ou alterar
 * recursos que nesse caso é um arquivo json e para o node e express entender
 * que o corpo foi repassado como json temos que avisar isso antes de todas as
 * requisições, vindo antes de todas as rotas app.use(express.json());
 * app.post('/users', (req, res) => {
 * 
 */

routes.post('/ongs', async (req, res) => {
  // acessando Query Params
  const queryParams = req.query;
  // acessando Route Params
  const routeParams = req.params;
  // acessando Route Body
  const bodyParams = req.body;

  console.log(queryParams);
  console.log(routeParams);
  console.log(bodyParams);
});
```
