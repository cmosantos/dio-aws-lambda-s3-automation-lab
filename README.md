# Executando Tarefas Automatizadas com Lambda Function e S3

Este repositório foi criado como parte de um desafio prático da DIO, com o objetivo de documentar os principais aprendizados sobre automação de tarefas utilizando AWS Lambda, Amazon S3, AWS CloudFormation e conceitos relacionados ao S3 Object Lambda.

A proposta do laboratório é consolidar conhecimentos sobre arquitetura serverless, processamento automatizado de objetos armazenados no Amazon S3 e uso de infraestrutura como código para provisionar recursos de forma mais segura, padronizada e reproduzível.

## Objetivo do Projeto

O objetivo deste projeto é organizar anotações, conceitos e insights adquiridos durante o estudo e a prática do laboratório, servindo como material de apoio para futuras implementações envolvendo automação na AWS.

Durante o desafio, foram estudados os conceitos de integração entre o Amazon S3 e o AWS Lambda, além do uso de templates do AWS CloudFormation para automatizar a criação e configuração de recursos necessários para uma arquitetura baseada em eventos e processamento sob demanda.

## Tecnologias e Serviços Estudados

Neste laboratório foram abordados os seguintes serviços e conceitos:

**Amazon S3**

O Amazon S3 é um serviço de armazenamento de objetos altamente escalável, utilizado para armazenar arquivos, documentos, imagens, backups, logs e diversos outros tipos de dados. No contexto deste laboratório, ele representa a camada de armazenamento onde os objetos ficam disponíveis para processamento.

**AWS Lambda**

O AWS Lambda é um serviço serverless que permite executar código sem a necessidade de provisionar ou gerenciar servidores. Ele pode ser acionado por eventos, como o envio de um arquivo para um bucket S3 ou uma solicitação feita por uma aplicação. Esse modelo facilita a automação de tarefas e reduz a complexidade operacional.

**AWS CloudFormation**

O AWS CloudFormation permite criar e gerenciar recursos da AWS por meio de templates declarativos. Com ele, é possível padronizar ambientes, reduzir erros manuais e reproduzir a infraestrutura de forma controlada.

**IAM**

O AWS Identity and Access Management é responsável pelo controle de permissões dentro da AWS. Em uma arquitetura envolvendo S3, Lambda e CloudFormation, o IAM é essencial para garantir que cada recurso tenha apenas as permissões necessárias para executar sua função.

**S3 Object Lambda**

O S3 Object Lambda permite adicionar lógica personalizada ao processo de recuperação de objetos no Amazon S3. Com ele, uma função Lambda pode modificar, filtrar, transformar ou processar dados antes que eles sejam retornados para uma aplicação.

## Funcionamento Conceitual da Solução

A arquitetura estudada no laboratório segue uma ideia simples: objetos armazenados no Amazon S3 podem ser acessados ou processados por meio de uma função Lambda. Essa função pode executar alguma lógica antes de devolver o conteúdo ao solicitante ou antes de concluir determinada tarefa automatizada.

Com o apoio do CloudFormation, a configuração dos recursos pode ser automatizada. Isso inclui a criação de pontos de acesso, funções Lambda, permissões IAM e demais componentes necessários para que a solução funcione corretamente.

De forma resumida, o fluxo conceitual pode ser representado assim:

1. Um objeto é armazenado ou acessado no Amazon S3.
2. Uma solicitação é direcionada para o ponto de acesso configurado.
3. O AWS Lambda é acionado para processar a solicitação.
4. A função Lambda executa a lógica definida.
5. O resultado é retornado para a aplicação ou usuário final.

## Principais Aprendizados

Durante o estudo deste laboratório, os principais aprendizados foram:

**Automação reduz erros manuais**

Ao utilizar CloudFormation, a criação dos recursos deixa de depender de configurações manuais no console da AWS. Isso torna o processo mais confiável, documentado e fácil de repetir.

**Lambda facilita arquiteturas orientadas a eventos**

O AWS Lambda permite criar soluções sob demanda, nas quais o código é executado apenas quando necessário. Esse modelo é útil para processamento de arquivos, transformação de dados, validações, geração de logs, integração com APIs e diversas outras tarefas automatizadas.

**Permissões IAM são parte central da arquitetura**

A integração entre S3, Lambda e CloudFormation depende diretamente de permissões bem configuradas. Um erro de permissão pode impedir que a função Lambda acesse objetos, grave respostas ou seja acionada corretamente.

**S3 pode ser mais do que armazenamento**

O Amazon S3 não precisa ser usado apenas como local de armazenamento. Com integrações serverless, ele pode fazer parte de fluxos automatizados de processamento, análise e entrega de dados.

**Documentação técnica também é entrega de projeto**

Além da implementação, documentar bem o que foi estudado é essencial. Um README organizado demonstra compreensão técnica, capacidade de comunicação e maturidade para registrar aprendizados de forma clara.

## Observação Sobre o S3 Object Lambda

Durante a pesquisa para este laboratório, foi identificado que o S3 Object Lambda passou por uma alteração de disponibilidade. Desde novembro de 2025, o serviço está disponível apenas para clientes existentes que já utilizavam o recurso e para parceiros selecionados da AWS Partner Network.

Mesmo assim, o estudo continua relevante porque os conceitos envolvidos, como processamento serverless, automação com Lambda, armazenamento com S3, permissões IAM e infraestrutura como código com CloudFormation, permanecem importantes para projetos em nuvem.

Para novos projetos, alternativas como Lambda acionado diretamente, API Gateway, Lambda Function URLs, CloudFront ou processamento no lado da aplicação podem ser consideradas, dependendo do cenário.

## Possíveis Casos de Uso

A arquitetura estudada pode ser aplicada em cenários como:

Processamento automático de arquivos enviados para um bucket S3.

Transformação de dados antes do consumo por uma aplicação.

Filtragem ou mascaramento de informações sensíveis.

Geração de versões personalizadas de arquivos.

Automação de pipelines simples baseados em eventos.

Integração entre armazenamento de objetos e funções serverless.

## Estrutura do Repositório

```text
dio-aws-lambda-s3-automation-lab/
│
├── README.md
└── notes/
    └── aprendizados.md
```

## Anotações Complementares

O arquivo `notes/aprendizados.md` pode ser utilizado para registrar observações adicionais feitas durante as aulas, comandos estudados, links úteis, dúvidas encontradas e possíveis melhorias para projetos futuros.

## Conclusão

Este laboratório reforçou a importância da automação em ambientes de nuvem. A combinação entre Amazon S3, AWS Lambda, IAM e CloudFormation mostra como é possível criar soluções mais organizadas, escaláveis e menos dependentes de configuração manual.

Mesmo quando o objetivo principal do desafio é documentar a experiência, o projeto ajuda a desenvolver uma habilidade muito importante para profissionais de tecnologia: transformar aprendizado prático em documentação clara, útil e compartilhável.

## Autor

Cláudio Menezes de Oliveira Santos

Projeto desenvolvido como parte dos desafios práticos da DIO.
