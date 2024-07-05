
# CI/CD com GitHub Actions

Trata-se de uma ferramenta do GitHub para gerenciamento de pipelines de integração e entrega contínua (CI/CD)

## Pipeline

Assim como um encanamento, são fluxos que vão seguir do ponto A até o ponto B executando diversas ações.

Todo processo manual, deve ser tornar uma pipeline automatizada para integração e entrega contínua.

## Integração Contínua (CI)

- Processo (Pipeline) de entrega de software em repositório.

    - Codificação
    - Commit
    - Build
    - Teste
    - Geração do pacote de entrega 

## Integação Contínua (CD)

- Processo (Pipeline) de entrega de software em ambiente de produção.

    - Início de uma Release
    - Teste
    - Aceite
    - Deploy em produção
    - Conclusão da Release

## O GitHub Actions

- **Workflow:** Fluxos de automatização para processos como CI, CD, atualização de certificados, etc.
- **Events:** Todo Workflow é estimulado por um evento disparado.
- **Jobs:** É um conjunto de tarefas executadas por um Workflow de forma paralela ou sequencial.
- **Steps:** São os passos que serão executados nos Jobs.
- **Actions:** Execuçao de algo que será executado no Job no formato yaml. Podemos usar Actions prontas ou criar as próprias.
- **Runners:** É o ambiente de execução, que pode ser Windows, Mac, Linux, Containers, etc.

### A Automação: Arquivo yaml

A configuração da automação por arquivo yaml pode ser customizada ou com templates ofertados pelo GitHub (Azure, AWS ECS, etc.)

#### Exemplo: Estrutura inicial "fake" de um Workflow

A estrutura abaixo demonstra um exemplo de estrutura básica de um workflow para geração de uma imagem Docker e publicação no Docker Hub.

```yml
name: Exemplo-Fake-CI-CD-Imagem-Docker
# Definição do evento que vai disparar a trilha
on:
  push: 
    branches: ["main"]
  # Permite a execução manual da automação
  workflow_dispatch: 

# Definição do conjuto de tarefas para execução do fluxo
jobs:
  # Job de integração contínua
  CI:
    # Definição do Runner onde será executado
    runs-on: ubuntu:latest
    # Ações que serão executadas para terminar o CI: Simula construção de uma imagem Docker
    steps:
      - name: Passo 01
        run: echo "Construir imagem Docker da aplicação"
      - name: Passo 02
        run: echo "Publicar a imagem Docker no Docker.Hub"

# Job de entrega contínua
  CD:
    # Definição do Runner onde será executado
    runs-on: ubuntu:latest
    # Gera dependência  da execução do step anterior para evitar a execução paralela
    needs: ["CI"]
    # Ações que serão executadas para terminar o CD: Simula a publicação da imagem Docker
    steps:
      - name: Passo 01
        run: echo "Deploy da aplicação"
```