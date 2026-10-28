# 📘 Atividade: Construindo APIs REST com FastAPI

## 🎯 Objetivo

Aprenda a criar uma API REST com FastAPI, definindo rotas HTTP, recebendo e validando dados e retornando respostas apropriadas. Ao final, você terá uma API para cadastrar e consultar livros.

## 📝 Tarefas

### 🛠️ Criar a estrutura inicial da API

#### Descrição
Crie uma aplicação FastAPI e implemente rotas simples para confirmar que a API está funcionando.

#### Requisitos
O programa concluído deve:

- Criar uma instância de `FastAPI`.
- Implementar `GET /` com uma resposta JSON de boas-vindas.
- Implementar `GET /health` com uma resposta que indique que a API está ativa.
- Permitir iniciar a aplicação com Uvicorn e acessar a documentação interativa em `/docs`.


### 🛠️ Implementar operações para livros

#### Descrição
Adicione rotas para consultar, cadastrar, atualizar e remover livros. Para manter o foco nas rotas REST, armazene os dados temporariamente em uma lista em memória.

#### Requisitos
O programa concluído deve:

- Implementar `GET /books` para listar os livros cadastrados.
- Implementar `GET /books/{book_id}` para consultar um livro pelo identificador.
- Implementar `POST /books` para cadastrar um livro.
- Implementar `PUT /books/{book_id}` para atualizar um livro existente.
- Implementar `DELETE /books/{book_id}` para remover um livro.
- Retornar o status HTTP `404 Not Found` quando o identificador não corresponder a um livro.


### 🛠️ Validar dados e respostas da API

#### Descrição
Use modelos do Pydantic para definir os dados aceitos e retornados pela API e configure os códigos de status HTTP para as operações.

#### Requisitos
O programa concluído deve:

- Definir um modelo de livro com campos como título, autor e ano de publicação.
- Validar os dados enviados ao cadastrar ou atualizar um livro.
- Retornar uma resposta de erro de validação quando os dados forem inválidos.
- Retornar `201 Created` ao cadastrar um livro.
- Documentar os campos e as respostas das rotas, de modo que apareçam na interface `/docs`.
