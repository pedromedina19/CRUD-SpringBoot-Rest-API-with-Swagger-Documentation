```markdown
# Documentação da API
- A API estará acessível em http://localhost:8080
- Está sendo usado como BD o postgresql, e o nome do banco de dados é product

## Autenticação

### POST /auth/login

Autentica um usuário e retorna um token.

**Corpo da requisição**:

```json
{
  "login": "usuario",
  "password": "senha"
}
```

### POST /auth/register

Registra um novo usuário.

**Corpo da requisição**:

```json
{
  "login": "usuario",
  "password": "senha",
  "role": "USER"
}
```

## Produtos

### GET /product

Retorna uma lista de todos os produtos ativos.

**Permissões**: Qualquer usuário autenticado.

### POST /product

Registra um novo produto.

**Corpo da requisição**:

```json
{
  "name": "Produto",
  "price_in_cents": 1000
}
```

**Permissões**: Apenas usuários com a função ADMIN.

### PUT /product

Atualiza um produto existente.

**Corpo da requisição**:

```json
{
  "id": "id-do-produto",
  "name": "Novo Nome",
  "price_in_cents": 2000
}
```

**Permissões**: Apenas usuários com a função ADMIN.

### DELETE /product/{id}

Deleta um produto.

**Permissões**: Apenas usuários com a função ADMIN.

## Documentação da API

A documentação completa da API pode ser encontrada em `http://localhost:8080/swagger-ui.html`.
```