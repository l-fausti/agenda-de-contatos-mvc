# 📱 Agenda de Contatos — ASP.NET Core MVC

Aplicação web para gerenciamento de contatos, desenvolvida com **ASP.NET Core MVC**. O projeto foi criado para praticar a arquitetura MVC, operações CRUD, Entity Framework Core, Razor Views, validação de formulários e estilização responsiva com Bootstrap e CSS.

> **Status:** projeto de estudo em evolução.

## ✨ Visão geral

A aplicação permite cadastrar e administrar contatos por meio das operações fundamentais de um CRUD:

- **Create:** cadastrar novos contatos;
- **Read:** listar e consultar os dados cadastrados;
- **Update:** editar informações existentes;
- **Delete:** excluir contatos após confirmação.

A interface utiliza uma identidade visual escura, navegação azul, cards, badges de status, formulários responsivos e efeitos de interação ao passar o cursor sobre os componentes.

## 🖥️ Telas da aplicação

### Página inicial

<img width="1349" height="943" alt="image" src="https://github.com/user-attachments/assets/2ef8c11f-75eb-4354-9cbd-e518fce05c4c" />

A página inicial apresenta a proposta da aplicação com uma navbar azul, um painel principal com a ilustração da agenda de contatos e cards que explicam os principais recursos do sistema.

### Listagem de contatos

<img width="1349" height="670" alt="image" src="https://github.com/user-attachments/assets/60be526a-2872-41a9-812f-645b922b5472" />

A tela exibe os contatos cadastrados em uma tabela responsiva, com informações de nome, telefone, status e ações para visualizar, editar ou excluir.

### Edição de contato

<img width="1350" height="762" alt="image" src="https://github.com/user-attachments/assets/c526b751-a674-4632-85bd-1a201b48f497" />

A tela de edição utiliza um formulário Razor com campos vinculados ao model `Contato`. Também possui um switch Bootstrap para indicar se o contato está ativo.

### Detalhes do contato

<img width="1408" height="664" alt="image" src="https://github.com/user-attachments/assets/c051867a-4152-4392-b794-92434a55f002" />

A tela de detalhes apresenta as informações de um contato individualmente, incluindo nome, telefone, status e ações para editar ou retornar à listagem.

<img width="1375" height="680" alt="image" src="https://github.com/user-attachments/assets/b0d62044-1006-4dd9-a4f1-f5cabf8dac15" />

A tela de exclusão é utilizada para confirmar a remoção definitiva de um registro. Ela foi pensada para evitar exclusões acidentais e reforçar a importância da ação.

🗂️ Estrutura principal

ProjetoMVC/
├── Context/
│   └── contexto e configuração do acesso aos dados
├── Controllers/
│   ├── ContatoController.cs
│   └── HomeController.cs
├── Migrations/
│   └── versões do banco geradas pelo Entity Framework Core
├── Models/
│   ├── Contato.cs
│   └── ErrorViewModel.cs
├── Views/
│   ├── Contato/
│   │   ├── Criar.cshtml
│   │   ├── Deletar.cshtml
│   │   ├── Detalhes.cshtml
│   │   ├── Editar.cshtml
│   │   └── Index.cshtml
│   ├── Home/
│   └── Shared/
│       ├── _Layout.cshtml
│       └── _ValidationScriptsPartial.cshtml
├── wwwroot/
│   ├── css/
│   │   └── site.css
│   ├── images/
│   │   └── contatos-app.svg
│   └── lib/
├── appsettings.json
├── Program.cs
└── ProjetoMVC.csproj


🛠️ Tecnologias utilizadas

C#;
ASP.NET Core MVC;
Entity Framework Core;
SQL Server;
Razor Views;
Bootstrap;
HTML5;
CSS3;
JavaScript.

⚙️ Como executar

Instale:
.NET SDK 8.0;
SQL Server ou SQL Server Express;
Visual Studio ou Visual Studio Code;
Entity Framework Core CLI, caso precise executar migrations manualmente

1. Clonar o repositório

git clone https://github.com/l-fausti/projeto-mvc-pratica.git
cd projeto-mvc-pratica

2. Restaurar as dependências

dotnet restore

3. Configurar o banco de dados

{
  "ConnectionStrings": {
    "DefaultConnection": "..."
  }
}

4. Aplicar migrations

dotnet ef database update

Caso o comando dotnet ef não esteja instalado:

dotnet tool install --global dotnet-ef

5. Executar a aplicação

dotnet watch run

🔄 Fluxo CRUD
Operação	Objetivo	Exemplo na aplicação
Create	Criar um registro	Formulário Criar
Read	Consultar registros	Index e Detalhes
Update	Alterar um registro	Formulário Editar
Delete	Remover um registro	Confirmação Deletar

📚 Conceitos praticados

separação de responsabilidades com MVC;
controllers e actions;
rotas e Tag Helpers;
requisições HTTP GET e POST;
model binding;
validação de modelos;
injeção de dependência;
Entity Framework Core e DbContext;
migrations;
persistência em SQL Server;
Views Razor;
layout compartilhado;
grid e componentes responsivos do Bootstrap;
organização de arquivos estáticos em wwwroot.





