# GitHub Actions .NET WebApp

Este repositório contém um exemplo de aplicação web .NET Core e um workflow configurado com GitHub Actions para construir, testar e implantar a aplicação automaticamente. Este projeto faz parte do Programa de Mentoria GitHub 4 Woman.

## Objetivo

O objetivo desta atividade é praticar os conceitos básicos do GitHub Codespaces e GitHub Actions, duas ferramentas poderosas oferecidas pelo GitHub para automação de construção, teste e implantação de código.

## Passos para Completar a Atividade

### 1. Criar um Repositório no GitHub

1. Crie um repositório no GitHub e nomeie-o como `github-actions-dotnet-webapp`.
2. Inicialize o repositório com um arquivo `README.md`.
3. Adicione um arquivo `.gitignore` e selecione o template do VisualStudio.

### 2. Criar o Código da Aplicação

1. Inicialize um Codespace.
   - Clique no botão “Code”.
   - Selecione a aba "Codespaces".
   - Clique no botão “Create codespace on main”.
   - Aguarde até que o setup esteja completo.

2. Crie uma aplicação web .NET Core usando os seguintes comandos no terminal:

   ```bash
   dotnet new webapp -n github4women
   dotnet restore **/*.csproj
   dotnet build **/*.csproj --no-restore
   dotnet run --project **/*.csproj

3. Criar o Arquivo de Workflow
- Criar um arquivo YAML para definir o workflow.
- Nomear como dotnet-build.yml
- salvar na pasta .github/workflows do repositório.

4. Configurar o Workflow
O arquivo YAML do workflow deve ser configurado para executar em duas ocasiões:
- Uma ação acionada por evento de push para o repositório.
- Outra ação agendada para ser executada a cada hora.
- Utilize pelo menos uma action pré-existente do GitHub e pelo menos um script personalizado.