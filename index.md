# Processos JHipster
[JHipster](http://www.jhipster.tech/) é uma ferramenta pra desenvolvimento de aplicações web. A plataforma implementa um gerador de código [Yeoman](http://yeoman.io/) pra criar aplicações baseadas na arquitetura [Spring Boot](http://projects.spring.io/spring-boot/) + [AngularJS](https://angularjs.org/) ou [Angular](https://angular.io/).

Esse framework será utilizado nesse disciplina para exemplificar (e praticar) alguns processos de desenvolvimento de software. Escolhemos um conjunto de processos que, de forma simplificada, abordam os principais fluxos de desenvolvimento de uma aplicação web.

Serão cinco os processos que iremos utilizar:
+ Configurando o ambiente de desenvolvimento
+ Criando uma aplicação
+ Criando um CRUD simples
+ Criando um CRUD complexo
+ Alterando um CRUD

## Configurando o ambiente

Esse processo os setup inicial do ambiente de desenvolvimento. Para realizar esse processo é necessário realizar as seguintes atividades:

1. Install Java 8 from the Oracle website.
1. (Optional) Install a Java build tool (Maven).
1. Install Git from git-scm.com. We recommend you also use a tool like SourceTree if you are starting with Git.
1. Install Node.js from the Node.js website (prefer an LTS version)
1. Install Yarn from the Yarn website
1. Install Yeoman: `yarn global add yo`
1. Only for AngularJS 1, install Bower: `yarn global add bower`
1. Only for AngularJS 1, install Gulp: `yarn global add gulp-cli`
1. Install JHipster: `yarn global add generator-jhipster`


![BPMN Processo 1](http://yuml.me/00ceb0b1)

## Criando uma aplicação (ou alterando as propriedades de uma aplicação)

Esse processo é usado para criar uma nova aplicação ou alterar algumas propriedades da aplicação. Normalmente é executado no início do processo de desenvolvimento e envolve definir a arquitetura da aplicação. Para realizar esse processo é necessário realizar as seguintes atividades:

1. Se for uma nova aplicação, criar o diretório da aplicação `mkdir myApp && cd myApp` 
1. Iniciar o gerador `jhipster`. O gerador irá fazer 15 perguntas (listadas abaixo):
1. Forneça valores apropriados para as 15 perguntas (quando se aplicar, usar o valor default sugerido pelo gerador)
1. Executar o comando `./mvnw`
1. (Opcional) Executar o comando `gulp`

![BPMN Processo 2](http://yuml.me/eabd15ea)

## Criando um CRUD simples

Esse processo é usado para criar um CRUD simples. Um CRUD é considerado simples quando o seu desenvolvimento pode ser feito a partir do próprio gerador `jhipster` (sem uso de uma modelagem de entidades). Normalmente os CRUDs dessa categoria são de Entidades com poucos atributos e associações. Para realizar esse processo é necessário realizar as seguintes atividades:

1. Sincronize o repositório de código local (faça o update e comite qualquer alteração)
1. Execute o comando `jhipster entity <NOME_ENTIDADE> --[options]`
1. Para cada atributo, forneça as seguintes informações: nome, tipo e regras para validação.
1. Para cada associação, forneça as seguintes informações: entidade associada, nome e tipo da associação.
1. O gerador irá fazer mais três perguntas , forneça a resposta default sugerida pelo gerador para as três.
1. Resolva os conflitos se existirem (indicando se deseja sobrescrever ou manter o código atual)
1. Reverta algumas alterações feitas pelo gerador (aquelas que sobrescrevem as alterações feitas pelo programador)
1. Implemente as customizações necessárias (tradução de mensagens, regras de negócio, código de teste, etc)
1. Faça o update do código e resolva os conflitos se existirem
1. Valide os testes com o código integrado
1. Comite as alterações


## Criando um CRUD complexo

Esse processo é usado para criar um CRUD complexo. Um CRUD é considerado complexo quando o seu desenvolvimento requer o uso de uma ferramenta de modelagem. Normalmente os CRUDs dessa categoria são de Entidades com vários atributos e associações. Para realizar esse processo é necessário realizar as seguintes atividades:

1. Desenhe o modelo no [JDL Studio](http://www.jhipster.tech/jdl-studio/)
1. Faça o download do arquivo no diretório `.jhipster`
1. Sincronize o repositório de código local (faça o update e comite qualquer alteração)
1. Execute o comando `jhipster import-jdl .jhipster/<NOMEDOARQUIVO>`
1. Resolva os conflitos se existirem (indicando se deseja sobrescrever ou manter o código atual)
1. Reverta algumas alterações feitas pelo gerador (aquelas que sobrescrevem as alterações feitas pelo programador)
1. Implemente as customizações necessárias (tradução de mensagens, regras de negócio, código de teste, etc)
1. Faça o update do código e resolva os conflitos se existirem
1. Valide os testes com o código integrado
1. Comite as alterações


## Alterando um CRUD

Esse processo é usado para alterar um CRUD (simples ou complexo). Para realizar esse processo é necessário realizar as seguintes atividades:

1. Altere o arquivo `.jhipster/<NOME_ENTIDADE>.json`
1. Sincronize o repositório de código local (faça o update e comite qualquer alteração)
1. Execute o comando `jhipster:entity <NOME_ENTIDADE> --regenerate` (`--skip-server` ou `--skip-client`)
1. Resolva os conflitos se existirem (indicando se deseja sobrescrever ou manter o código atual)
1. Reverta algumas alterações feitas pelo gerador (aquelas que sobrescrevem as alterações feitas pelo programador)
1. Implemente as customizações necessárias (tradução de mensagens, regras de negócio, código de teste, etc)
1. Faça o update do código e resolva os conflitos se existirem
1. Valide os testes com o código integrado
1. Comite as alterações
