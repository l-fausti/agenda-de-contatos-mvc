📱 CRUD de Contatos — ASP.NET Core MVC

Projeto desenvolvido com o objetivo de praticar e consolidar conceitos fundamentais do desenvolvimento web utilizando o padrão arquitetural MVC (Model-View-Controller).

A aplicação consiste em um sistema simples de gerenciamento de contatos, permitindo realizar as principais operações de um CRUD (Create, Read, Update e Delete), com persistência dos dados em um banco de dados SQL Server.

O projeto foi desenvolvido com foco no aprendizado de conceitos utilizados no desenvolvimento de aplicações web com o ecossistema .NET, buscando aplicar uma estrutura organizada e próxima de cenários encontrados em projetos reais.

🎯 Objetivos do projeto
Praticar o padrão arquitetural MVC;
Compreender a separação de responsabilidades entre Model, View e Controller;
Implementar operações de CRUD;
Trabalhar com persistência de dados utilizando Entity Framework Core;
Realizar integração com SQL Server;
Desenvolver páginas utilizando Razor Views;
Trabalhar com rotas, formulários e requisições HTTP;
Aplicar conceitos básicos de validação de dados;
Organizar o projeto seguindo uma estrutura adequada para aplicações ASP.NET Core.
🚀 Funcionalidades

A aplicação permite:

📋 Listar contatos cadastrados;
🔎 Visualizar informações de um contato;
➕ Cadastrar novos contatos;
✏️ Editar contatos existentes;
🗑️ Excluir contatos;
✅ Validar informações inseridas nos formulários;
💾 Persistir os dados no SQL Server.
🛠️ Tecnologias utilizadas
C#
ASP.NET Core MVC
Entity Framework Core
SQL Server
Razor
HTML5
CSS3
🏗️ Arquitetura

O projeto utiliza o padrão MVC (Model-View-Controller), separando a aplicação em diferentes responsabilidades.

Model

Responsável por representar as entidades e os dados utilizados pela aplicação.

Neste projeto, a principal entidade é o Contato, que representa as informações de cada contato cadastrado.

View

Responsável pela interface apresentada ao usuário.

As Views são construídas utilizando Razor, permitindo apresentar os dados enviados pelos Controllers e criar formulários para interação com a aplicação.

Controller

Responsável por receber as requisições HTTP, executar as regras necessárias e determinar qual resposta deve ser apresentada ao usuário.

As ações do Controller realizam operações como:

Listagem de contatos;
Cadastro;
Edição;
Visualização;
Exclusão.
🗄️ Persistência de dados

A persistência é realizada utilizando o Entity Framework Core, que permite trabalhar com o banco de dados por meio de objetos e classes C#.

O projeto utiliza o SQL Server como banco de dados.

O Entity Framework Core é responsável pelo mapeamento entre as entidades da aplicação e as tabelas do banco de dados, utilizando o conceito de ORM (Object-Relational Mapping).

📂 Estrutura do projeto
📦 Contatos
 ┣ 📂 Controllers
 ┃ ┗ 📄 ContatosController.cs
 ┣ 📂 Data
 ┃ ┗ 📄 ApplicationDbContext.cs
 ┣ 📂 Models
 ┃ ┗ 📄 Contato.cs
 ┣ 📂 Views
 ┃ ┗ 📂 Contatos
 ┃   ┣ 📄 Index.cshtml
 ┃   ┣ 📄 Details.cshtml
 ┃   ┣ 📄 Create.cshtml
 ┃   ┣ 📄 Edit.cshtml
 ┃   ┗ 📄 Delete.cshtml
 ┣ 📄 appsettings.json
 ┣ 📄 Program.cs
 ┗ 📄 Contatos.csproj

A estrutura pode variar conforme a evolução do projeto, mas a organização busca manter cada responsabilidade em seu respectivo local.

🔄 Operações CRUD

O projeto utiliza as quatro operações fundamentais de manipulação de dados:

Operação	Descrição
Create	Cadastra um novo contato
Read	Consulta e exibe os contatos
Update	Atualiza os dados de um contato
Delete	Remove um contato
📚 Conceitos praticados

Durante o desenvolvimento foram praticados conceitos importantes do ecossistema .NET, como:

Arquitetura MVC;
Controllers e Actions;
Models;
Razor Views;
Routing;
HTTP GET e POST;
Entity Framework Core;
DbContext;
Migrations;
Relacionamento entre aplicação e banco de dados;
SQL Server;
Model Binding;
Validação de modelos;
Injeção de Dependência;
Operações assíncronas com async/await;
Organização de projetos ASP.NET Core.
⚙️ Como executar o projeto
Pré-requisitos

Antes de executar a aplicação, é necessário ter instalado:

.NET SDK
SQL Server
Visual Studio ou Visual Studio Code
Entity Framework Core CLI, caso necessário para executar as migrations
1. Clone o repositório
git clone https://github.com/seu-usuario/projeto-mvc-pratica.git
2. Acesse a pasta do projeto
cd seu-repositorio
3. Configure a conexão com o SQL Server

No arquivo appsettings.json, configure a ConnectionString de acordo com o ambiente local:

{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=ContatosDb;Trusted_Connection=True;TrustServerCertificate=True;"
  }
}
4. Execute as migrations
dotnet ef database update
5. Execute a aplicação
