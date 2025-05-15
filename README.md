# Estrutura do Projeto - MVC e Endpoints

Este projeto segue o padrão **MVC (Model-View-Controller)**, que ajuda a deixar o código mais organizado e fácil de manter. Aqui vai um resumo do que cada parte faz:

---

## Models

Os models são os arquivos que lidam direto com o banco de dados. Cada entidade (aluno, curso, professor, usuário) tem seu próprio model.

Eles fazem coisas como:

- Buscar todos os registros
- Criar novos dados
- Atualizar ou deletar registros

Exemplo: o `aluno.js` tem funções para listar alunos, adicionar um novo, editar e até mostrar quais alunos pertencem a um curso.

---

## Controllers

Os controllers recebem as requisições que o usuário faz na aplicação (por exemplo, ao clicar em "Cadastrar aluno") e falam com os models para realizar as ações necessárias.

Temos controladores como:

- `homeController`: mostra a página inicial
- `alunoController`: cuida de tudo que envolve alunos
- `cursoController`: adiciona, edita ou remove cursos
- `professorController`: gerencia professores
- `userController`: entrega uma API em JSON para manipular usuários

---

## Endpoints

Esses são os “caminhos” que o navegador ou o frontend usam para interagir com o sistema.

Alguns exemplos:

- `/alunos` → lista os alunos
- `/alunos/:id` → edita um aluno
- `/cursos` → adiciona um curso
- `/professores` → mostra todos os professores
- `/users` → endpoint de API para listar ou criar usuários (formato JSON)

---

## Resumindo

- **Model**: cuida do banco de dados  
- **Controller**: decide o que fazer com cada requisição  
- **Endpoint**: o endereço que o usuário acessa para fazer algo no sistema

Essa estrutura facilita muito a organização do projeto, principalmente quando ele começa a crescer.

