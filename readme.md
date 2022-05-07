### ToDos 

---

### Requsitos

- [x] Deve ser possivel crir um usuário
- [] Deve ser possivel buscar um usuário
- [] Deve ser possivel inserir um todo em um usuário
- [] Deve ser possivel buscar os todos por usuário
- [] Deve ser possivel alterar o titulo ou deadline em um todo
- [] Deve ser possivel marcar o todo como concluído
- [] Deve ser possivel deletar um todo

---

### Regras de negócio

- [] Não deve ser possivel crir um usuário quando o username já estiver em uso
- [] Não deve ser possivel criar um todo sem um usuário

---

### Model fields

- User { id: 'uuid', name, username, todos:[] }
    - create (POST /users)
- ToDos { id: 'uuid', done: false, title, deadline: new date, created_at: new date }
    - create (POST /todos (header: username))
    - find todo (GET /todos (header: username))
    - Update todos (PUT /todos/:id (header: username))
    - Upadate done (PATCH /todos/:id/done (header: username))
    - Delete todo (DELETE /todos/:id (header: username))