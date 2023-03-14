<h2 align="left">
  📊 O que é BIGQUERY? E como utilizar na prática?
</h2>

[Nesse vídeo](https://youtu.be/3zjOLUNBFeY) eu mostro o que é o BigQuery e como você pode utilizar para analisar seus dados.

Bom, no começo quando entrei na minha primeira oportunidade de tecnologia, eu precisei aprender mais sobre ferramentas da Cloud da Google e o BigQuery foi a principal delas. 

## ✨ O que é BigQuery?

##### 📚 [DOCUMENTAÇÃO OFICIAL](https://cloud.google.com/bigquery/docs?hl=pt-br)

De maneira simplificada, se você ou sua empresa tiver uma pequena quantidade de dados, você pode armazenar em uma planilha, mas a medida que a quantidade de dados vai crescendo para gigabytes, terabytes ou mesmo pentabytes, você pode começar a precisar de um sistema mais eficiente, como um Data Warehouse. Isso porque todos esses dados não são muito úteis, a menos que você tenha uma forma de analisar eles.

Em resumo, o Bigquery é um serviço de armazenamento de dados que permite fazer análise de grandes quantidades de dados, em escala de pentabytes, do **GOOGLE CLOUD**. É um data warehouse totalmente gerenciado e sem servidor, ou seja, permite que voce se concentre em analises ao invés de gerenciar a infraesturutra. Além disso você também não vai precisar configurar ou instalar nada e também não precisa de um administrador de banco de dados. você apenas abre o navegador, faz o login e começa a usar.

Trabalhar com os dados no Bigquery vai envolver 3 etapas principais:

- **ARMAZENAMENTO:** os dados são armazenados em uma tabela estruturada, o que significa que você pode usar o SQL padrão para facilitar a consulta e a análise de dados.
- **INGESTÃO:** você pode fazer upload de dados do cloud storage, importar dados de varios formatos de arquivo, conectar ao Vertex AI, fazer streming de dados do Cloud Dataflow.
- **CONSULTA:** quando os dados estiverem no Bigquery, você pode tentar responder algumas perguntas. O Bigquery é compativel com Linguagem de consulta estruturada, ou SQL. 


## 🕵️‍♀️ BigQuery na prática:

Para demonstração no vídeo, eu usei a base de dados do IMDB (sites de críticas de filmes e séries do mundo): [Clique aqui pra conferir a base de dados disponível no Kaggle](https://www.kaggle.com/datasets/omarhanyy/imdb-top-1000)

No vídeo, busquei responder as seguintes questões:

1. Quantos filmes foram lançados por ano?

```
SELECT COUNT(Series_Title) as Count_Series, Released_Year FROM `noted-acronym-368113.youtube.imdb1000`
GROUP BY Released_Year
ORDER BY Count_Series DESC
```

2. Qual a média de classificações por ano de lançamento?


```
SELECT ROUND(AVG(IMDB_Rating),2) as IMDB_Rating, Released_Year FROM `noted-acronym-368113.youtube.imdb1000`
GROUP BY Released_Year
ORDER BY Released_Year DESC
```

Obrigada por acompanhar até aqui! Se gostou e foi útil, [não esquece de se inscrever no canal](https://www.youtube.com/channel/UC7C3taM54q4rsEIDPFNVsLg) e até o próximo vídeo!👋
