# 🧠 Perguntas para medir aprendizado 

1. **Explique com suas palavras o papel de cada camada da arquitetura MVC usada neste projeto.**  
   *Como o Model, o Controller e a View interagem entre si?*

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

## Views
Os views são a interface do servidor com o usuário. Eles servem para enviar pacotes de JSON para o backend. Recebem rotas e mostram ao usuário as informações.

Exemplo: `aluno.ejs`

---  

2. **Como ocorre o envio e o recebimento de dados no formato JSON neste projeto?**  
   *Cite uma rota que responde em JSON e explique seu funcionamento.*
   
   ```javascript
   router.post('/', controller.store);
   ```
   Essa rota, por exemplo, guia para o Controller do Aluno, levando as informacões em JSON que serão convertidas em uma requisicao para o banco de dados no Model. Esse criará um novo aluno na tabela aluno.

3. **Qual a importância de usar HTML básico com formulários e tabelas para organizar e manipular dados no navegador?**  
   *Por que esse tipo de estrutura ainda é útil em projetos back-end com Node.js?*

      Esse tipo de estrutura ainda eh útil por que da a possibilidade de verificar todas as funcionalidades do sistema sem precisar mexer com tecnologias mais complexas, que sim, geram resultados melhores, mas que tomariam muito mais tempo para *debugar*.