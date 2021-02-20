# Kafka como plataforma de stream de dados distribuído em real time
Analytics/Kafka/KSql/Zabbix/Python/kSQL/Influx

## Motivação
Utilizar o kafka como plataforma de mensageria distribuida e stream de dados em tempo real

## Desafio
* Implementação e configuração da strutura do kafka, kSqldb, Grafana, Influx
 
## Abordagem
Desenvolver uma aplicação em pyhton que assine informações púbidas de negociação e oferta de bitcoin e etherium atravês de websockets disponibilizado pela exchange Binance e envie para um tópico expecífico no kafka, os tópicos são utilizados como base para a criação de streams de dados e tabelas para o tratamento e organização da informação pelo kSql, a partir de então os dados são enviados continuamente para o influx como time series 

1. Desenvolvimento de Producer e Consumer em Python;
2. Criação de tópicos no Kafka
3. Criação de stream de dados e tabelas via kSql;
4. Criação de estrutura de time series no Influx;
5. Criação de dashboards via Grafana;


## Solução
1. Modelagem de estruturas de tabela otimizadas em um novo schema de banco de dados Oracle de forma a suportar a carga e a performance exigida por uma solução de analytics
	- SQL
	- Airflow
	- Oracle
	- Modelagem

2. Desenvolvimentos de ETL's em Airflow e Python que conectam ao schema do banco de dados Oracle do ERP de produção e fazem todo o tratamento e conversão dos diversos tipos de dados para carga em um outro schema de banco de dados também em Oracle otimizado para trazer uma performance satisfatória
	- Python
	- Airflow
	- Oracle
	- SQL

3. Desenvolvimento de dashboard sob a plataforma Metabase que aborda diversas métricas de negócio utilizando filtros dinâmicos para refinar as visualizações 
	- SQL
	- Metabase
	
## Estruturação da Solução
<p align="center">
	<img src="etl-airflow-metabase.jpg" height="70%" width="70%">
</p>

## Resultado
A área de negócio passa a ter uma visão global, precisa e dinâmica de varios indicadores de negócio que interagem entre sí, tais como: Posição de Compras, Previsão de Recebimento, Previsão de Vendas, Indicadores de Estoque, etc., desta forma é possível tomar decisões estratégicas de forma a garantir que a companhia seja cada vez mais competitiva e eficiente



<img src="https://github.com/wscardua/kafka-python-grafana-influx/blob/main/Consumer_Producer_log.gif" width="450"/>

<img src="https://github.com/wscardua/kafka-python-grafana-influx/blob/main/CryptoDash.gif" width="450"/>

