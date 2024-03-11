# Git e GitHub

## O que é Git

Git é um sistema de controle de versões distribuído, gratuito e de código aberto, projetado para lidar com projetos de pequena a grande escala com rapidez e eficiência. Ele permite que múltiplos desenvolvedores trabalhem juntos em um mesmo projeto sem confusões.

## O que é GitHub

GitHub é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando Git. Ele proporciona várias funcionalidades como gerenciamento de projetos, integração contínua, feedback de código e várias outras, facilitando a colaboração entre desenvolvedores.

## Opções ao GitHub

- **GitLab:** Oferece repositórios privados gratuitos e é auto-hospedado, proporcionando controle total sobre os dados.
- **AWS CodeCommit:** Serviço de controle de versão gerenciado pela Amazon, oferece integrações com outros serviços da AWS.
- **BitBucket:** Focado em equipes profissionais, oferece integrações com o Trello e o Jira, além de repositórios privados gratuitos para equipes pequenas.

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

## Repositório

Um repositório no Git é uma coleção de arquivos de um projeto e o histórico de todas as mudanças feitas nesses arquivos. Repositórios podem ser locais, armazenados no seu computador, ou remotos, hospedados em uma plataforma como GitHub.

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

