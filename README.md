# Plataforma ALUMNI - UNISANTOS

A **Plataforma ALUMNI** é uma iniciativa desenvolvida no contexto acadêmico da **Universidade Católica de Santos (UNISANTOS)**, com o objetivo de fortalecer o vínculo entre alunos, ex-alunos, docentes e gestores da Universidade.

A plataforma busca criar um ambiente digital **interativo e colaborativo**, onde os egressos possam:

- Se reconectar com a universidade;
- Acompanhar atualizações sobre os cursos;
- Compartilhar experiências profissionais;
- Acessar oportunidades no mercado de trabalho.

Com isso, promove-se a **conexão e o intercâmbio de conhecimento** entre os membros da comunidade acadêmica.

## Desenvolvimento

O projeto é desenvolvido por alunos do curso de **Ciência da Computação da UNISANTOS** e está sendo atualmente aprimorado por dois grupos do **7º semestre**. A missão dos grupos é implementar melhorias contínuas para a construção da plataforma.

A **Product Owner (PO)**, **Lilian Marques**, do setor de Relações Públicas, é responsável por guiar o desenvolvimento e garantir que o projeto atenda às necessidades da comunidade acadêmica. Ela atua como elo entre os alunos desenvolvedores e os usuários finais da plataforma, assegurando que o sistema seja:

- Funcional;
- Intuitivo;
- Alinhado aos objetivos institucionais.

## Público-Alvo e Benefícios

A principal comunidade beneficiada pelo projeto são os **alunos e ex-alunos da UNISANTOS**, especialmente os que passaram pelos cursos da área de **Tecnologia da Informação**.

A plataforma também representa um canal estratégico para **empresas e organizações parceiras**, que poderão:

- Divulgar vagas de estágio e emprego;
- Estabelecer parcerias com a universidade.

Dessa forma, a Plataforma ALUMNI contribui não apenas para o fortalecimento do vínculo entre egressos e a instituição, mas também para a **inserção profissional dos alunos no mercado de trabalho**.

## Metodologia

O projeto adota uma abordagem **iterativa**, baseada na coleta de feedbacks da comunidade acadêmica para garantir **melhorias contínuas** no sistema.

## Saiba Mais

Para saber mais sobre a UNISANTOS e suas iniciativas acadêmicas, acesse o site oficial da instituição:

👉 [https://www.unisantos.br](https://www.unisantos.br)


# Criação do Feed
Integrantes:\
-Alec Emil Meier\
-Adrielle Valascvijus Fernandes\
-Daniel Domingues Gama\
-Gustavo Andrade\
-Henry Mitsuo Kasai\
-Lavínia Lopes de Lana\
-Leonardo Wright Lima\
-Matheus Gois Rocha\
-Matheus Moledo Fonseca Vasconcelos\
-Michael Douglas Santos Costa\
-Raquel Nazaré Belfort Costa\
-Thiago Conrado Martins

## Alterações
  Criação da página de feed com as funcionalidades de buscar postagens e inserir postagens.\
  Ao abrir a página é realizada uma requisição ao back-end buscando as postagens em ordem decrescente da data da postagem e retornado ao front-end para serem exibidas.\
  Contudo, é possível observar que a integração com o banco de dados foi realizada de forma local e a estrutura de usuários ainda não foi criada, e por isso está sendo exibido uma imagem padrão na foto do usuário, assim com um nome padrão.
  
## Sugestões de Melhoria
-Criação da estrutura de usuários, assim como a integração deles com o banco de dados;\
-Inserção de novas funcionalidades sobre as postagens. Exemplo: editar, excluir, curtir, comentar, compartilhar;\
-Inserir novos tipos de postagens. Exemplo: evento, enquete, inserção de imagens.

# Criação e Autenticação do Feed Alumni
Integrantes:\
-Alec Emil Meier\
-Adrielle Valascvijus Fernandes\
-Daniel Domingues Gama\
-Gustavo Andrade\
-Henry Mitsuo Kasai\
-Lavínia Lopes de Lana\
-Leonardo Wright Lima\
-Matheus Gois Rocha\
-Matheus Moledo Fonseca Vasconcelos\
-Michael Douglas Santos Costa\
-Raquel Nazaré Belfort Costa\
-Thiago Conrado Martins

Este projeto implementa a criação da estrutura de autenticação segura (Cadastro e Login) e conexão com o banco de dados local.

## Alterações
Criação da a arquitetura de autenticação completa, essencial para a segurança da plataforma:\
-Entidade de Usuário: Criação da estrutura de usuários (User) no Doctrine (Back-end) com campos obrigatórios (email_user, password, etc.).\
-Cadastro (/sign-up): Implementação de uma API (POST /api/users/create_user) que utiliza o Symfony Password Hasher para criptografar senhas antes de salvar no banco de dados.\
-Login (/sign-in): Implementação de uma API de login segura (POST /api/users/login) que busca o usuário por e-mail e verifica a senha (texto plano) contra o hash armazenado no banco de dados, utilizando o PasswordHasher.\
-Gerenciamento de Estado Global (Contexto): Gerenciamento dos dados do usuário logado na página persistindo durante a navegação (entre as páginas de Feed, Perfil, etc.). O UserContext, um Contexto React, foi estabelecido para gerenciar o estado global user e setUser. Após o login ou cadastro, o userId é persistido no localStorage.

## Sugestões de Melhoria Futuras
-Inserção de Novas Funcionalidades nas Postagens: Exemplo: editar, excluir, curtir, comentar, compartilhar.\
-Criação de Página do perfil com as funcionalidades de edição dos dados de usuário e inserção de imagem como foto de perfil.\
-Inserção de validações na página de cadastro de usuário (exemplo: verificação de força da senha, confirmação de senha, confirmação de email, verificação de cpf já existente).
