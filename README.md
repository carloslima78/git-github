# Git e GitHub

## O que é Git

Git é um sistema de controle de versões distribuído, gratuito e de código aberto, projetado para lidar com projetos de pequena a grande escala com rapidez e eficiência. Ele permite que múltiplos desenvolvedores trabalhem juntos em um mesmo projeto sem conflitos.

## O que é GitHub

GitHub é uma plataforma de hospedagem de código fonte e arquivos com controle de versão baseada em Git que proporciona várias funcionalidades como gerenciamento de projetos, integração e entrega contínua (CI/CD), feedback de código e várias outras, facilitando a colaboração entre desenvolvedores.

## Alternativas ao GitHub

- **GitLab:** Oferece repositórios privados gratuitos e é auto-hospedado, proporcionando controle total sobre os dados.
- **AWS CodeCommit:** Serviço de controle de versão gerenciado pela AWS, oferece integrações com outros serviços deste provider.
- **BitBucket:** Focado em equipes profissionais, oferece integrações com o Trello e o Jira, além de repositórios privados gratuitos para equipes pequenas.
- **Google Cloud Source Repositories:** Serviço de hospedagem de repositórios privados na nuvem do Google, integra-se com o Cloud Build e o Pub/Sub para automatizar pipelines de CI/CD.
- **Azure Repos:** Parte do Azure DevOps, oferece repositórios Git privados ilimitados e gratuitos, suporta grandes arquivos Git (Git LFS) e integra-se com as ferramentas do Azure DevOps para CI/CD.

## Instalando e Configurando o Git no Ubuntu

- Instala o Git

```bash
sudo apt update
sudo apt install git
```

- Verifica a instalação do Git

```bash
git --version
```

- Adiciona o nome de usuário nas configurações do Git para identificar cada comando executado

```bash
git config --global user.name "username"
```

- Adiciona o e-mail de usuário nas configurações do Git para identificar cada comando executado

```bash
git config --global user.email "username"
```

- Lista as configurações presentes no Git 

```bash
git config --global --list
```

## Repository (Repositório)

Um repositório no Git é uma coleção de arquivos de um projeto e o histórico de todas as mudanças feitas nesses arquivos. Repositórios podem ser locais, armazenados no seu computador, ou remotos, hospedados em uma plataforma como GitHub.

## Project (Projeto)

Um projeto no GitHub é um espaço para organizar e gerenciar arquivos, códigos e recursos relacionados a um trabalho específico. Ele pode conter pastas, arquivos, issues, pull requests e wikis, proporcionando um ambiente centralizado para colaboração e controle de versão do seu trabalho.

Um "project" (projeto) no GitHub pode ser usado para gerenciar o backlog de tarefas, semelhante ao que é feito em metodologias ágeis como o Scrum. É possível criar colunas para representar diferentes etapas do processo de desenvolvimento, como "To Do" (A fazer), "In Progress" (Em progresso), "Testing" (Testando), "Done" (Feito), entre outras, dependendo das necessidades do seu projeto.

Dentro dessas colunas, você pode criar "cards" (cartas) que representam tarefas específicas, como novas funcionalidades, correção de bugs, ou qualquer outra atividade relacionada ao desenvolvimento do software. Os cards podem ser movidos entre as colunas à medida que progridem no processo.

## Repository vs Project

A diferença entre um "project" (projeto) e um "repository" (repositório) no GitHub é que um projeto é um espaço de organização para gerenciar e visualizar informações, como issues, notas, e tarefas relacionadas a um trabalho específico. Por outro lado, um repositório é onde os arquivos e códigos reais do projeto são armazenados. 

Enquanto o repositório contém o código-fonte e o histórico de versões, o projeto fornece uma maneira de organizar e acompanhar o progresso do trabalho, incluindo tarefas, marcos, e colaboradores. Em resumo, o repositório é o local onde o código é armazenado, e o projeto é o espaço para gerenciar o andamento e as tarefas relacionadas a esse código.

### Exemplo

Suponhamos que estejamos trabalhando em um projeto de desenvolvimento de um site:

1. **Repositório** (Repository):
- O repositório é onde todo o código do site é armazenado.
- Você cria um repositório chamado "meu-site" no GitHub para este projeto.
- Todos os arquivos HTML, CSS, JavaScript e outras assets do site são armazenados neste repositório.
- Os commits (registros de alterações) são feitos no repositório sempre que você adiciona ou altera o código.

2. **Projeto** (Project):
- Você cria um projeto chamado "Desenvolvimento do Site" no GitHub.
- Dentro deste projeto, você tem colunas como "To Do" (A fazer), "In Progress" (Em progresso), e "Done" (Feito).
- Cada carta (card) no projeto representa uma tarefa ou uma funcionalidade a ser implementada no site.
- Você pode mover as cartas entre as colunas conforme avança no desenvolvimento do site.
- O projeto fornece uma visão visual do progresso do desenvolvimento, sem lidar diretamente com o código.

Na prática:

#### Repositório "meu-site":
- Contém arquivos do site (index.html, style.css, script.js, etc.)
- Commits registrados quando alterações são feitas no código.

#### Projeto "Desenvolvimento do Site":
- **To Do** (A fazer):
  - Criar página inicial
  - Estilizar o menu de navegação
- **In Progress** (Em progresso):
  - Implementar funcionalidade de formulário de contato
- **Done** (Feito):
  - Adicionar imagens à galeria de fotos

## Commit

Um commit no Git é como uma fotografia de todos os arquivos do seu projeto em um ponto específico no tempo. É uma maneira de registrar as mudanças feitas no repositório e incluir uma mensagem explicativa sobre o que foi feito.

## Stages

Quando se trabalha com Git, os arquivos no seu repositório passam por três estágios principais antes de serem efetivamente registrados no histórico do repositório. Esses estágios são:

- **Modified:** Neste estágio, o arquivo foi alterado no seu diretório de trabalho, mas ainda não foi preparado para ser commitado. Isso significa que Git reconhece que o arquivo foi alterado, mas essas alterações ainda não estão marcadas para serem incluídas no próximo commit.
- **Staging:** Após modificar um arquivo, o próximo passo é colocá-lo no estágio de "Staging". Isso é feito usando o comando *git add [nome-do-arquivo]* ou *git add .* para adicionar todas as alterações de uma vez. Neste estágio, os arquivos estão prontos para serem commitados. O "Staging" é como uma pré-visualização ou uma área de preparação onde você define exatamente o que vai entrar no próximo commit.
- **Commited:** Uma vez que os arquivos estão no estágio de "Staging" e você está satisfeito com as mudanças, o próximo passo é commitar essas alterações. Isso é feito usando o comando git commit, que move os arquivos do estágio de "Staging" para o estado "Commited". Isso significa que as alterações foram oficialmente registradas no histórico do Git. O commit cria um ponto na história do seu projeto que você pode voltar a qualquer momento, se necessário.

Esses estágios facilitam o gerenciamento das suas mudanças e permitem que você controle exatamente o que será incluído em cada commit, ajudando a manter um histórico de projeto limpo e compreensível.

## Branch

Branches (ou "ramificações") no Git são utilizadas para trabalhar em diferentes versões de um repositório ao mesmo tempo. Cada branch representa uma linha independente de desenvolvimento. O branch padrão no Git é o "master", mas é comum criar novos branches para desenvolver novas funcionalidades ou corrigir bugs, antes de mesclar essas mudanças de volta ao branch principal.

## Criando um Repositório


```bash
mkdir projeto-1
cd projeto-1
```

```bash
git init
ls -a
```

## Incluindo arquivos no Stage

- Criando o arquivo *index.html* no repositório.

```bash
cd projeto-1
touch index.html
git status
```

- **Resultado:** Arquivos ainda não rastreados e controlados pelo Git, estágio **Modified**.

```bash
carlos@ubuntu-Lenovo-IdeaPad-Z400:~/Documents/projeto-1$ git status
No ramo master

No commits yet

Arquivos não monitorados:
  (utilize "git add <arquivo>..." para incluir o que será submetido)
        index.html
```

- Adicionando o arquivo *index.html* no controle Git

```bash
git add index.html
git status
```

- **Resultado:** As alterações estão prontas para serem comitadas, estágio **Staging:**.

```bash
carlos@ubuntu-Lenovo-IdeaPad-Z400:~/Documents/projeto-1$ git status
No ramo master

No commits yet

Mudanças a serem submetidas:
  (utilize "git rm --cached <arquivo>..." para não apresentar)
        new file:   index.html
```

- Removendo o arquivo para o estágio anterior, caso haja arrependimento.

```bash
git git rm --cached index.html
git status
```

- **Resultado:** O arquivo volta ao estágio anterior **Modified**

```bash
carlos@ubuntu-Lenovo-IdeaPad-Z400:~/Documents/projeto-1$ git status
No ramo master

No commits yet

Arquivos não monitorados:
  (utilize "git add <arquivo>..." para incluir o que será submetido)
        index.html
```

## Realizando Commit

- Comitando o arquivo index.html.

```bash
git commit -m "Adicionado arquivo index"
git status
```

- Adicionando um novo arquivo.

```bash
touch estilo.css
git status
```

```bash
git add estilo.css
git status
```

ou 

```bash
git add .
git status
```

- Comitando o novo arquivo estilo.css.

```bash
git commit -m "Adicionado arquivo de estilo css"
git status
```

- Verificando o log completo.

```bash
git log
```

- Resultado

```bash
carlos@ubuntu-Lenovo-IdeaPad-Z400:~/Documents/projeto-1$ git log
commit 74650f2754e8288ed1dda859aff517d105f9e17e (HEAD -> master)
Author: carloslima78 <carlos.lima78@gmail.com>
Date:   Sat Mar 16 18:14:49 2024 -0300

    Adicionado arquivo de estilo css

commit 2bb3a3919ee2e82ca09696ec9e89c24107896c4f
Author: carloslima78 <carlos.lima78@gmail.com>
Date:   Sat Mar 16 18:13:22 2024 -0300

    Adicionado arquivo index
```

- Verificando o log em uma linha.

```bash
git log --oneline
```

- Resultado

```bash
carlos@ubuntu-Lenovo-IdeaPad-Z400:~/Documents/projeto-1$ git log --oneline
74650f2 (HEAD -> master) Adicionado arquivo de estilo css
2bb3a39 Adicionado arquivo index
```

## Revertendo um Commit

### Comando Checkout

O comando *Checkout* ...

- Lista o histórico de commits realizados

```bash
git log --oneline
```

- Resultado

```bash
carlos@ubuntu-Lenovo-IdeaPad-Z400:~/Documents/projeto-1$ git log --oneline
1b69a2e (HEAD -> master) Adicionado subtitulo no html
b7fd354 Adicionado titulo no html
a142461 Adicionado cor de fundo
16cbd63 Ajuste no index.html
74650f2 Adicionado arquivo de estilo css
2bb3a39 Adicionado arquivo index
```

- Voltando ao commit *16cbd63* com o comando **checkout**.

```bash
git checkout 16cbd63
```

Como resultado, o arquivo retorna para a versão presente no commit *16cbd63*.

```bash
carlos@ubuntu-Lenovo-IdeaPad-Z400:~/Documents/projeto-1$ git log --oneline
16cbd63 (HEAD) Ajuste no index.html
74650f2 Adicionado arquivo de estilo css
2bb3a39 Adicionado arquivo index
```

### Comando Revert

O comando *Revert* ...


### Comando Reset

O comando *Reset* ...

## Ignorando Arquivos

- Adicionando um suposto arquivo para variáveis de ambiente que deseja-se ignorar.

```bash
touch .env
git status
```

```bash
git status
No ramo master
Arquivos não monitorados:
  (utilize "git add <arquivo>..." para incluir o que será submetido)
        .env
        .gitignore
```

- Adicionando o arquivo gitignore, onde adicionaremos o arquivo *.env*

```bash
touch .gitignore
git status
```

- Após adicionar o arquivo *.env* no arquivo *.gitignore*, o arquivo das variáveis não será mais listado, e logo não será rastreado pelo Git.

```bash
git status
No ramo master
Arquivos não monitorados:
  (utilize "git add <arquivo>..." para incluir o que será submetido)
        .gitignore
```

## Criando Branches

- Lista as branches, neste caso termos apenas a principal *Master*.

```bash
git branch
```

- Cria uma nova branch a partir da principal

```bash
git branch nova-branch
```

- Entra na nova branch usando o comando *checkout* que também serve para trocar de branch.

```bash
git checkout nova-branch
```
- Adiciona um novo arquivo na nova branch

```bash
touch javascript.js
git add .
git commmit -m "Novo arquivo adicionado"
```

### Caso necessite remover uma Branch

- Removendo uma branch

```bash
git branch -d nova-branch
```

- Removendo uma de mandeira forçada, pois o comando anterior pode barrar a remoção caso seja uma branch ... 

```bash
git branch -D nova-branch
```

## Realizando o Merge entre Branchs

Neste passo faremos o processo de merge entre branchs, onde a branch *Master* é o destino e a branch *nova-branch* será a origem.

- Seguir para a branch principal, em nosso caso a *Master*.

```bash
git checkout master
```

- Realizar o merge da branch de origem para a branch de destino, onde passará a ter todos os arquivos da origem.

```bash
git merge nova-branch
```

- Após realizar o comando cima, a branch *Master* passa a ter os arquivos da branch *nova-branch*.

```bash
carlos@ubuntu-Lenovo-IdeaPad-Z400:~/Documents/projeto-1$ git merge mercado-pago
Updating 26e150d..dfaba2d
Fast-forward
 mercado-pago.js | 2 ++
 1 file changed, 2 insertions(+)
```

## Atribuindo um Autor a um Commit

É uma boa prática quanto se têm diversos desenvolvedores trabalhando no mesmo repositório.

```bash
git commit -m "Algum ajuste" --author="Carlos <carlos@mail.com>"
```

## Pull Request (PR)

Um Pull Request (PR) é um mecanismo fundamental no controle de versão de um projeto, especialmente em sistemas de controle de versão distribuídos, como o Git. É um processo no qual o desenvolvedor sugere alterações que fez em um repositório Git para serem incorporadas à versão principal do projeto.

Funcionamento Básico

1. **Criação de uma Branch:** Antes de iniciar o trabalho em uma nova funcionalidade ou correção de bugs, é recomendado criar um novo branch em seu repositório local. Isso mantém as alterações separadas da branch principal (geralmente chamada de main ou master).

```bash
git checkout -b nova-branch
```

2. **Commit das Alterações:** Após fazer suas alterações no código, o desenvolvedor precisa commitá-las no seu branch local.

```bash
git add .
git commit -m "Descrição das alterações"
```
3. **Push para o Repositório Remoto:** Agora o desenvolvedor tem as alterações no seu branch local, mas elas ainda não estão disponíveis para os outros colaboradores do projeto. Para isso, será necessário enviar seu branch e commits para o repositório remoto (como GitHub, GitLab, etc.).

```bash
git push origin nova-branch
```

4. **Abertura do Pull Request:** Uma vez que o branch com as alterações está no repositório remoto, o desenvolvedor pode abrir um Pull Request. Isso significa que está solicitando que as alterações feitas no  branch sejam "puxadas" para a branch principal do projeto.

- Vá até a página do repositório no GitHub (ou plataforma semelhante).
- Selecione o branch e clique em "New Pull Request".
- Escreva uma descrição detalhada das suas alterações, explicando o que foi feito e por quê.
- Os colaboradores do projeto podem revisar suas alterações, fazer comentários e sugerir ajustes antes de incorporar as alterações na branch principal.

5. **Revisão e Merge:** Os colaboradores revisam o seu Pull Request, discutem as alterações propostas e, se tudo estiver correto, o Pull Request é "merged" (fundido) na branch principal. Isso significa que suas alterações agora fazem parte oficialmente do projeto.

## Fork: Colaborando com projetos abertos

Em projetos de código aberto, o conceito de "fork" é essencial para permitir a colaboração de diversos desenvolvedores em um mesmo projeto. Um fork é uma cópia independente de um repositório, geralmente hospedado em um serviço como GitHub, GitLab, ou Bitbucket. 

Quando o desenvolvedor "forka" um repositório, cria-se uma cópia do projeto completo em sua própria conta, permitindo que faça alterações sem afetar o repositório original.

