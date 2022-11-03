<center><img src="https://avatars.githubusercontent.com/u/91892865?s=200&v=4" /></center>

## Seja Bem-Vindo à SPA!
Estamos felizes de ter você no nosso processo seletivo para Equipe de Desenvolvimento.

Nesse processo, vamos analisar seu conhecimento sobre APIs Rest, Jest, Typescript e Git!

### Como enviar o desafio

Crie um repositório público no [GitHub](https://github.com). Assim que finalizar seu desafio, envie o link do repositório para o endereço de email `code@spa-br.com`

Lembre-se que estamos analisando seu conhecimento Git também, então utilize [Commits Semânticos](https://blog.geekhunter.com.br/o-que-e-commit-e-como-usar-commits-semanticos/) no processo de desenvolvimento do desafio.

ex:

* Caso esteja desenvolvendo o endpoint de Usuários, crie uma branch chamada `feature/endpoint-usuarios`;
* Faça os commits semânticos nela, ex: `feat(Usuários): Criando endpoint GET de usuários`;
* Quando finalizar, realize o merge para a branch `main`.

### Dúvidas sobre o desafio

Caso tenha alguma dúvida sobre o desafio, [abra uma issue](https://github.com/DevTeamSPA/desafio-dev/issues) neste repositório e alguém da nossa equipe de desenvolvimento vai te ajudar! Utilizamos as issues para que cada dúvida possa servir de ajuda para o próximo!

A seguir, está seu desafio, boa sorte!

## DESAFIO

Resumo:
* Criar um Banco de dados PostgreSQL
* Criar uma api para consumir o banco de dados utilizando TypeORM como ORM

Diferenciais:

Você deverá usar o `express` como servidor e o `typeorm` como ORM. Você poderá usar ou não Docker. Fica ao seu critério.

### Instruções:

## 1. Criar um banco PostgreSQL

### 1.1 Criar as tabelas:

User
| coluna   | tipo    |        descrição         |
|----------|---------|--------------------------|
| id       | int     | Chave primária da tabela |
| nome     | varchar | Nome de usuário          |
| email    | varchar | E-mail de usuário        |
| password | varchar | Senha de acesso          |
| status   | int     | 0 - Inativo, 1 - Ativo   |

UserInfo
| coluna   | tipo    |        descrição         |
|----------|---------|--------------------------|
| id       | int     | Chave primária da tabela |
| idUser   | int     | id do Usuário (fk)       |
| telefone | varchar | Telefone do Usuário      |
| endereco | text    | Endereço do Usuário      |
| admin    | int     | 0 - User, 1 - Admin      |
| status   | int     | 0 - Inativo, 1 - Ativo   |

## 2. Criar primeiramente os testes da aplicação utilizando `jest`

### 2.1 Desenvolver uma API Restful para cada resource:
~~~html
- Usuários

[GET]         /usuarios              - Lista todos os usuários
[GET]         /usuarios/:id          - Busca uma Categoria por id
[POST]        /usuarios              - Cria um Usuário
[PATCH]       /usuarios/:id          - Edita um Usuário
[DELETE]      /usuarios/:id          - Delete um Usuário (deve atualizar o UserInfo setando idUser como NULL para funções que utilizam essa tabela)

Quando um usuário é criado, deve ser criado um UserInfo com o id do usuário que foi criado e inserido em idUser para futuras atualizações
~~~

## Boa sorte!
Atenciosamente, Equipe SPA
