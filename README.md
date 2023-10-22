# Desafio 01 - Fundamentos de Node.js
Esse desafio faz parte do módulo 1 da trilha de Node.js do Ignite da Rocketseat.

## Sobre a aplicação
A aplicação é uma API desenvolvida em Node.js para realizar um CRUD de *tasks* (tarefas). Com a aplicaão é possível criar uma nova tarefa, listar todas as tarefas, atualizar uma tarefa, remover uma tarefa, marcar tarefas como concluídas e importar tasks através de um arquivo .CSV.

## Requisitos funcionais (RF)
- [x] Deve ser possível criar uma task
- [x] Deve ser possível listar todas as tasks
- [x] Deve ser possível listar uma task pelo `id`
- [x] Deve ser possível remover uma task pelo `id`
- [x] Deve ser possível marcar pelo `id`uma task como completa
- [x] Deve ser possível importar tasks em massa por um arquivo CSV

## Regras de Negócio (RN)
- [x] A estrutura de uma task deve ser:
    - `id` - Identificador único de cada task
    - `title` - Título da task
    - `description` - Descrição detalhada da task
    - `completed_at`- Data que a task foi concluída. O valor inicial deve ser `null`
    - `created_at` - Data de quando a task foi criada
    - `updated_at` - Deve ser sempre alterado para a data de quando a task foi atualizada

## Rotas da aplicação
- `POST - /tasks` - Deve ser possível criar uma task no banco de dados, enviando os campos `title` e `description` por meio do `body` da requisição.
Ao criar uma task, os campos: `id`, `created_at`, `updated_at` e `completed_at` devem ser preenchidos automaticamente, conforme a orientação das propriedades acima.

- `GET - /tasks` - Deve ser possível listar todas as tasks salvas no banco de dados.
Também deve ser possível realizar uma busca, filtrando as tasks pelo `title` e `description`

- `PUT - /tasks/:id` - Deve ser possível atualizar uma task pelo `id`.
No `body` da requisição, deve receber somente o `title` e/ou `description` para serem atualizados.
Se for enviado somente o `title`, significa que o `description` não pode ser atualizado e vice-versa.
Antes de realizar a atualização, deve ser feito uma validação se o `id` pertence a uma task salva no banco de dados.

- `DELETE - /tasks/:id` - Deve ser possível remover uma task pelo `id`. Antes de realizar a remoção, deve ser feito uma validação se o `id` pertence a uma task salva no banco de dados.

- `PATCH - /tasks/:id/complete` - Deve ser possível marcar a task como completa ou não. Isso significa que se a task estiver concluída, deve voltar ao seu estado “normal”. Antes da alteração, deve ser feito uma validação se o `id` pertence a uma task salva no banco de dados.

## Como executar a aplicação
Para executar a aplicação siga os seguintes passos:

- Clone e acesse o repositório:
```
https://github.com/andersondev96/ignite-nodejs2023-desafio01-fundamentos-nodejs
```
```
cd ignite-nodejs2023-desafio01-fundamentos-nodejs
```

- Instale as dependências do projeto:
```
npm install
```
 
- Execute o projeto com o comando:
```
npm run dev
```
- O servidor irá rodar na porta `localhost:3333`

## Licença

Este projeto está sob a licença [MIT](LICENSE).

## Autor

<img src="https://avatars.githubusercontent.com/u/49786548?v=4" width="64" style="border: 2px solid blue; border-radius: 50px" />

**Anderson Fernandes Ferreira**

[![instagram](https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/anderson_ff13)
[![email](https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white)](mailto:andersonfferreira96@gmail.com.br)
[![linkedin](https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/anderson-fernandes96/)

Feito com 💚 por Anderson Fernandes 👋 [Entre em contato!](https://www.linkedin.com/in/anderson-fernandes96/)