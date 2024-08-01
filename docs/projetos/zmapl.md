---
tags:
  - Zabbix
  - API
  - Angular
  - Node.js
  - OTRS
---
# ZmapL
Mapeando eventos de um mesmo host no Zabbix para abrir ticket com diferentes caracteristicas.

## **Motivação:**

Durante nosso trabalho recente com o Zabbix, identificamos a necessidade de que um mesmo host abra tickets automaticamente, mas com características distintas baseadas em seu nome. Essa necessidade surgiu devido ao nosso ambiente de Veeam, que gerencia jobs de vários clientes diferentes. Quando um chamado é gerado automaticamente, gostaríamos que ele fosse categorizado corretamente com o nome do cliente e o serviço apropriado.

## **Solução:**

Consideramos algumas abordagens, como segmentar os jobs em múltiplos hosts no Zabbix, com cada host dedicado a um cliente específico. No entanto, essa solução complicaria a organização e a inclusão de novos clientes. Assim, optamos por uma abordagem mais eficiente: utilizamos um arquivo JSON como um "DE/PARA" que mapeia o JOB com um prefixo e define as características que o chamado deve ter. Contudo, manter e atualizar esse arquivo JSON sempre que um cliente é adicionado, removido ou modificado, especialmente com várias pessoas envolvidas, pode ser propenso a erros.

Para resolver esse problema, desenvolvemos uma aplicação web que facilita o gerenciamento desse arquivo. A solução foi criada usando Angular para o frontend, Node.js para o backend e MySQL para o banco de dados. Toda a infraestrutura está containerizada com Docker e pode ser visualizada [aqui para o frontend](https://hub.docker.com/repository/docker/kmpc2013/zmaplfront/general) e [aqui para o backend](https://hub.docker.com/repository/docker/kmpc2013/zmaplback/general).

## **Benefícios:**

Com essa solução, qualquer usuário pode acessar o portal, chamado ZmapL (abreviação de Zabbix Map to Ligero), para realizar as ações necessárias. Isso traz mais facilidade, agilidade e reduz significativamente a incidência de erros.