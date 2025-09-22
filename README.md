> **AVISO:** O conteúdo deste documento foi organizado e estruturado com o auxílio de uma Inteligência Artificial. No entanto, todo o conhecimento, insights e anotações aqui presentes são de autoria própria, refletindo minha compreensão e aprendizado durante as aulas do módulo.

# Executando Tarefas Automatizadas com Lambda e S3

### 1. Visão Geral do Projeto

Este repositório documenta o estudo sobre a criação de um fluxo de trabalho de automação serverless na AWS. O objetivo é utilizar o **Amazon S3** como gatilho (trigger) para acionar uma **AWS Lambda Function**, que executa uma tarefa pré-definida. Todo o ambiente foi simulado localmente com o **AWS LocalStack** para facilitar o desenvolvimento.

### 2. Amazon S3 (Simple Storage Service)

O Amazon S3 é um serviço de armazenamento de objetos em nuvem, projetado para ser altamente seguro, durável e escalável.

* **Funcionalidades:** Atua como um repositório para backups e armazenamento de qualquer tipo de objeto (arquivos, imagens, etc.), permitindo o acesso aos dados de qualquer lugar.
* **Ciclo de Vida:** Possui diferentes classes de armazenamento (tiers), movendo objetos menos acessados do "hot" (acesso frequente) para classes mais baratas como o "Glacier" (arquivamento).
* **Segurança:** Permite a implementação de regras de segurança detalhadas para controlar o acesso aos dados.

**Principais Vantagens:**
* **Disponibilidade:** Alta disponibilidade dos dados.
* **Escalabilidade:** Capacidade de armazenar quantidades massivas de dados.
* **Durabilidade:** Projetado para uma durabilidade de 99.999999999% (onze noves).
* **Segurança:** Recursos robustos de criptografia e controle de acesso.

### 3. AWS Lambda

AWS Lambda é um serviço de computação **serverless** (sem servidor) que executa código em resposta a eventos, sem a necessidade de gerenciar servidores manualmente.

* **Funcionamento:** O desenvolvedor simplesmente "sobe o código" e a AWS cuida de todo o resto. A função é executada quando um evento (como um upload de arquivo no S3) ocorre.
* **Escalabilidade:** Escala automaticamente conforme a demanda, desde algumas requisições por dia até milhares por segundo.

**Principais Vantagens:**
* **Execução sob Demanda:** O código só é executado quando necessário.
* **Escalabilidade Automática:** Não é preciso se preocupar com a capacidade dos servidores.
* **Custo Eficiente:** O pagamento é feito apenas pelo tempo de computação consumido, em milissegundos.
* **Integração:** Integra-se nativamente com dezenas de outros serviços da AWS.

### 4. AWS LocalStack

LocalStack é um simulador de ambiente AWS de código aberto (*open source*) que roda localmente na máquina do desenvolvedor.

* **Objetivo:** Seu principal propósito é simular um ambiente de nuvem AWS, permitindo que os desenvolvedores criem, testem e depurem suas aplicações sem precisar se conectar à nuvem real.
* **Fluxo de Trabalho:** O desenvolvedor cria e testa a solução no ambiente local (com LocalStack) e, uma vez que tudo está funcionando, envia a aplicação para a nuvem AWS real.
* **Pré-requisito:** Requer a instalação do Python para funcionar.
