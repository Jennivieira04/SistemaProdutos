# Sistema de Gerenciamento de Produtos

API REST desenvolvida em Java com Spring Boot para gerenciamento de produtos.

## Tecnologias utilizadas

- Java 25
- Spring Boot 4.1.1
- Spring Data JPA
- Hibernate
- PostgreSQL
- Maven
- Swagger / OpenAPI
- Postman
- IntelliJ IDEA

## Funcionalidades

- Cadastro de produtos
- Listagem de produtos
- Busca de produto por ID
- Busca de produtos por nome
- Atualização de produtos
- Exclusão de produtos
- Validação de dados
- Tratamento de erros
- Persistência em banco de dados PostgreSQL
- Documentação interativa com Swagger

## Endpoints

### Cadastrar produto

`POST /produtos`

Exemplo:

```json
{
  "nome": "Notebook Gamer",
  "preco": 4500.00,
  "quantidade": 3
}
```

### Listar produtos

`GET /produtos`

### Buscar produto por ID

`GET /produtos/{id}`

Exemplo:

`GET /produtos/1`

### Buscar produto por nome

`GET /produtos/buscar?nome=Notebook`

### Atualizar produto

`PUT /produtos/{id}`

Exemplo:

```json
{
  "nome": "Notebook Gamer",
  "preco": 5000.00,
  "quantidade": 4
}
```

### Excluir produto

`DELETE /produtos/{id}`

## Banco de dados

O projeto utiliza PostgreSQL.

Banco:

```text
sistema_produtos
```

Configuração local:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/sistema_produtos
spring.datasource.username=postgres
spring.datasource.password=SUA_SENHA
```

> Substitua `SUA_SENHA` pela senha configurada no seu PostgreSQL apenas no arquivo local `application.properties`. Não coloque a senha real neste README.

## Documentação da API

Com a aplicação em execução, a documentação pode ser acessada em:

`http://localhost:8080/swagger-ui.html`

## Como executar o projeto

1. Instale o Java 25.
2. Instale o PostgreSQL.
3. Crie o banco `sistema_produtos`.
4. Configure a senha do usuário `postgres` no `application.properties`.
5. Abra o projeto no IntelliJ IDEA.
6. Execute `SistemaProdutosApplication`.
7. Acesse a documentação pelo Swagger.

## Status do projeto

Versão inicial concluída e publicada no GitHub.