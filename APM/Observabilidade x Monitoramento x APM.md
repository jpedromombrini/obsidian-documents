Dentro da arquitetura de software temos alguns conceitos que parecem ser sinônimos mas precisamos defini-los. Os conceitos são: Observabilidade, Monitoramento e APM. Vamos à definição deles.

**Observabilidade**
É um conceito mais amplo e representa a capacidade de entender o que está acontecendo dentro de um sistema, baseado nas saídas que esse sistema oferece, por exemplo logs, métricas e traces.
- Métricas  - dados numéricos, como uso de CPU, tempo de resposta(o APM registra que um endpoint da API `/carrinho` passou de 200ms para 2s de tempo de resposta nos últimos 10 minutos).
- Logs - Registros detalhados de eventos que ocorreram(ocorreu uma exceção `TimeoutException` em uma consulta ao banco de dados).
- Traces - Rastreamento do caminho de uma requisição dentro do sistema(requisição está demorando mais especificamente no trecho que faz a chamada para a tabela `ProdutosEstoque`).

Juntando essas três informações, a equipe consegue **não só saber que algo está errado (monitoramento), mas entender exatamente onde, por que e como resolver (observabilidade)**.

APM é parte da observabilidade, porque coleta e correlaciona métricas, logs e traces para fornecer visibilidade sobre o desempenho da aplicação.

**Monitoramento**
É o ato de coletar e exibir dados em tempo real, normalmente com alertas definidos.
Ele responde a perguntas como:
- Está funcionando?
- Está lento?
- O serviço caiu?

Ou seja monitoramento é uma prática dentro da observabilidade, mas não fornece contexto profundo sobre o "porquê" de um problema - esse é o papel da observabilidade.

APM(Application Performance Monitoring)
É uma solução de observabilidade com foco em aplicações, que:
- Monitora desempenho de endpoints, banco de dados, serviços externos.
- Detecta gargalos, erros e falhas automaticamente.
- Correlaciona logs, métricas e traces.

**Resumindo:**

|Conceito|Escopo|Foco principal|
|---|---|---|
|Observabilidade|Amplo|Entendimento profundo do sistema|
|Monitoramento|Subconjunto da observabilidade|Dados e alertas em tempo real|
|APM|Subconjunto da observabilidade|Desempenho e comportamento de aplicações|

