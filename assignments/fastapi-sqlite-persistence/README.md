# 📘 Atividade: Persistência com SQLite em APIs FastAPI

## 🎯 Objetivo

Substitua o armazenamento temporário em memória da API de livros por um banco SQLite, usando o módulo `sqlite3` do Python. Você aprenderá a criar uma tabela e executar operações CRUD que mantêm os dados disponíveis mesmo após reiniciar a aplicação.

## 📝 Tarefas

### 🛠️ Criar o banco de dados e a tabela de livros

#### Descrição
Prepare o armazenamento persistente da API criando um arquivo de banco de dados SQLite e uma tabela para os livros.

#### Requisitos
O programa concluído deve:

- Usar o módulo `sqlite3` da biblioteca padrão do Python.
- Criar ou abrir um arquivo de banco de dados SQLite.
- Criar uma tabela `books` com identificador, título, autor e ano de publicação.
- Criar a tabela automaticamente quando a aplicação iniciar, sem apagar os dados já existentes.


### 🛠️ Conectar as rotas da API ao SQLite

#### Descrição
Atualize as rotas da API de livros criada na atividade anterior para consultar e cadastrar livros no banco de dados, em vez de usar uma lista em memória.

#### Requisitos
O programa concluído deve:

- Implementar `GET /books` para retornar os livros armazenados no SQLite.
- Implementar `GET /books/{book_id}` para consultar um livro pelo identificador.
- Implementar `POST /books` para inserir um livro no banco e retornar o livro criado.
- Usar consultas SQL parametrizadas para inserir e consultar dados.
- Manter os modelos Pydantic e as respostas HTTP apropriadas da API anterior.


### 🛠️ Completar as operações CRUD persistentes

#### Descrição
Conclua a integração implementando a atualização e a remoção de livros e confirme que os dados continuam disponíveis após reiniciar a aplicação.

#### Requisitos
O programa concluído deve:

- Implementar `PUT /books/{book_id}` para atualizar um livro existente no SQLite.
- Implementar `DELETE /books/{book_id}` para remover um livro do SQLite.
- Retornar `404 Not Found` quando uma operação procurar um identificador inexistente.
- Confirmar que os livros cadastrados permanecem disponíveis após encerrar e iniciar novamente a aplicação.
- Fechar as conexões com o banco de dados após seu uso.
