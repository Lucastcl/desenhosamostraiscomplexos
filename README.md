# Desenhos Amostrais Complexos

**Projeto de Iniciação Científica (PIBIC 2025-26)**  
**Orientadora:** Alinne de Carvalho Veiga  
**Aluno:** {nome dos alunos}

Este repositório contém o código-fonte e o texto da apostila didática sobre planos amostrais complexos.

---

## Guia de Contribuição

Este guia fornece instruções detalhadas sobre como configurar o RStudio para colaborar com este projeto, clonar o repositório e enviar suas atualizações.

### Pré-requisitos
Para seguir este guia, você precisará ter instalado em seu computador:
1.  **R** e **RStudio**.
2.  **Git** (Sistema de controle de versão).
3.  Uma conta no **GitHub**.

---

### Passo 1: Conectar o RStudio ao GitHub

Para conseguir baixar e, principalmente, enviar alterações para o GitHub, você precisa conectar seu RStudio à sua conta. A forma mais segura e recomendada é utilizando um **Token de Acesso Pessoal (PAT)**.

**1. Gerar o Token no GitHub**
1.  Abra o RStudio.
2.  No Console (painel inferior esquerdo), instale o pacote `usethis`:
    ```r
    install.packages("usethis")
    ```
3.  Execute o seguinte comando:
    ```r
    usethis::create_github_token()
    ```
4.  Uma página do GitHub abrirá no seu navegador. Faça login se solicitado.
5.  Em "Note", dê um nome para identificar seu computador (ex: "RStudio Casa").
6.  Em "Expiration", defina uma validade (recomendado: 90 dias ou "No expiration" se o computador for pessoal e seguro).
7.  Certifique-se de que a caixa **repo** (Full control of private repositories) está marcada.
8.  Role até o final e clique em **Generate token**.
9.  **COPIE O CÓDIGO GERADO** (ele começa com `ghp_`). 
    *Atenção: Você não conseguirá vê-lo novamente após sair dessa página.*

**2. Salvar o Token no RStudio**
1.  No RStudio, instale o pacote `gitcreds`:
    ```r
    install.packages("gitcreds")
    ```
2.  Execute o comando:
    ```r
    gitcreds::gitcreds_set()
    ```
3.  O console pedirá uma senha/token ("Enter password or token"). **Cole o código que você copiou** e aperte Enter.

Pronto! Seu RStudio agora tem permissão para interagir com seus repositórios no GitHub.

---

### Passo 2: Clonar o Repositório (Baixar o Projeto)

Você pode trabalhar neste projeto de duas formas: como um **Colaborador Direto** (sem fork) ou via **Contribuição Externa** (com fork).

**Opção A: Colaborador Direto (Recomendado para a equipe)**
Para usar este método, o dono do repositório deve ter adicionado seu usuário do GitHub como "Collaborator" nas configurações do projeto. Isso permite que você edite e envie mudanças diretamente.

1.  No RStudio, vá no menu **File** > **New Project...**
2.  Selecione **Version Control** > **Git**.
3.  No campo "Repository URL", cole o link oficial deste projeto:
    `https://github.com/Lucastcl/desenhosamostraiscomplexos.git`
4.  Em "Create project as subdirectory of", escolha a pasta onde o projeto será salvo no seu computador.
5.  Clique em **Create Project**.

**Opção B: Contribuição Externa (Fork)**
Se você não faz parte da equipe oficial e não tem permissão de escrita, você deve antes fazer um "Fork" (uma cópia) do projeto.
1.  Clique no botão **Fork** no canto superior direito desta página no GitHub.
2.  Siga os mesmos passos da Opção A, mas use o link do **seu** repositório copiado (ex: `https://github.com/SEU_USUARIO/desenhosamostraiscomplexos.git`).

---

### Passo 3: Fluxo de Trabalho (Editar e Atualizar)

Com o projeto aberto no RStudio:

1.  **Edite:**
    Navegue pela aba "Files" e abra os arquivos `.Rmd` (capítulos) para escrever ou corrigir o texto. Salve as alterações.

2.  **Visualize (Build):**
    Para verificar como o livro está ficando, vá na aba **Build** (geralmente no painel superior direito) e clique no botão **Build Book**. O livro será gerado e aberto em uma janela de visualização.

3.  **Salve as Alterações (Commit):**
    Quando terminar uma etapa do trabalho:
    *   Vá para a aba **Git** no RStudio.
    *   Marque as caixas na coluna "Staged" ao lado dos arquivos que você alterou.
    *   Clique no botão **Commit**.
    *   Escreva uma mensagem clara descrevendo o que foi feito (ex: "Revisão do capítulo 2").
    *   Clique em **Commit**.

4.  **Envie para a Nuvem (Push):**
    *   Ainda na aba Git, clique no botão **Push** (seta verde para cima).
    *   Se você seguiu o Passo 1 corretamente, o envio será feito automaticamente.

*Nota aos usuários da Opção A:* Suas alterações já estarão online no projeto oficial!
*Nota aos usuários da Opção B:* Você precisará ir ao GitHub e abrir um "Pull Request" para sugerir suas mudanças ao projeto original.
