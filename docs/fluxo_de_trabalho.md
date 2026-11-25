# Fluxo de trabalho no Git/Github
## 1. Crie a issue no Kanban
1. No inicio do [repositório](https://github.com/guilhermefrmdev/comanda-link), entre na guia [Projects](https://github.com/guilhermefrmdev/comanda-link/projects).
2. Entre no Kanban e crie a Issue relacionado com usa tarefa no **Backlog**.

    ```
    A Issue deve seguir o padrão:

    ### Tipo de Alteração
    - [ ] Correção de Bug
    - [ ] Documentação
    - [ ] Funcionalidade ou Recurso
    - [ ] Testes
    - [ ] Refatoração

    ### O vai ser feito
    - Item 1
    - Item 2
    - Item 3
    ```

3. Na aba lateral Development da Issue, crie a branch em que você irá trabalhar. Obs: Utilize o padrão de branch do [Conventional Branch](https://conventionalbranch.org/pt-br/)
4. Ao iniciar o desenvolvimento, mova a Issue para **In Progress**.

## 2. Desenvolvendo
1. Desenvolva a sua tarefa.
2. Utilize o padrão de commit do [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)

## 3. Entregando
1. Após de desenvolver sua tarefa, faça o `git push` da sua branch.
2. Faça um Pull Request, descrevendo o que foi feito.

    ```
    A Pull Request deve seguir o padrão:

    ### Tipo de Alteração
    - [ ] Correção de Bug
    - [ ] Documentação
    - [ ] Funcionalidade ou Recurso
    - [ ] Testes
    - [ ] Refatoração

    ### O que foi feito
    - Item 1
    - Item 2
    - Item 3
    ```
3. Mova sua Issue para **In review**.
4. O Pull Request deve ter o review de no mínimo uma outro desenvolvedor antes de ser realizado o merge na branch main.
5. Espere seu PR ser revisado e mergeado na main.