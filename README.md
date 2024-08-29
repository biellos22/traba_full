#
<h5 align='center'> Difícil porém difícil</h5>

#

<h4>Atividade Prática: Implementação de um Sistema de Cadastro, Login e Gerenciamento de Usuários com JWT e Banco de Dados Relacional</h4>

Objetivo:
O objetivo desta atividade é desenvolver um sistema completo de autenticação e gerenciamento de usuários utilizando um 
banco de dados relacional (MySQL ou PostgreSQL) e JSON Web Token (JWT). O sistema deve permitir o cadastro, login, atualização, deleção e listagem de usuários.
Descrição:
Os alunos deverão implementar uma aplicação web usando Node.js, Express, 
Sequelize (ou outro ORM relacional) e JWT. A aplicação deve atender aos seguintes requisitos:
#
Requisitos Funcionais:
Cadastro de Usuário:
A aplicação deve permitir que um novo usuário se cadastre fornecendo username, email, e password;
A senha deve ser armazenada no banco de dados de forma segura utilizando hash (bcrypt).
#
Login de Usuário:
A aplicação deve permitir que um usuário faça login utilizando email e password;
Um token JWT deve ser gerado e retornado ao usuário em caso de sucesso no login;
O token deve expirar em 1 hora.
#
Listagem de Usuários:
A aplicação deve fornecer uma rota protegida que permita a listagem de todos os usuários cadastrados;
Apenas usuários autenticados (portadores de um token JWT válido) devem ter acesso a essa rota.
#
Atualização de Usuário:
A aplicação deve permitir que um usuário atualize seu username e email;
Apenas o próprio usuário pode atualizar suas informações;
A senha não deve ser atualizada nesta rota.
#
Deleção de Usuário:
A aplicação deve permitir que um usuário delete sua própria conta;
Apenas o próprio usuário pode deletar sua conta.
#
Proteção das Rotas:
Todas as rotas, exceto as de cadastro e login, devem ser protegidas por autenticação JWT;
O token JWT deve ser enviado no cabeçalho Authorization como Bearer <token>.
#
Banco de Dados Relacional:
Use um banco de dados relacional (MySQL ou PostgreSQL);
Utilize Sequelize ou outro ORM de sua escolha para interagir com o banco de dados;
Crie um modelo de User com as colunas: id, username, email, password, createdAt, updatedAt.
#
Autenticação:
Utilize JWT para a autenticação dos usuários;
Armazene o segredo do JWT e outras configurações sensíveis em um arquivo .env.
#
Estrutura do Projeto:
Organize o projeto em pastas: models, routes, controllers, middlewares;
Crie middlewares para proteger as rotas e verificar a validade do token JWT;
Criar o .env para variáveis de ambiente.
