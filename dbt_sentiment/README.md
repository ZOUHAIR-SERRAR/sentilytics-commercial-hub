# Projet Analyse de Sentiment - Reseaux Sociaux

## Description
Pipeline complet qui correle les mentions Twitter avec les ventes.

## Lancement rapide

### 1 - Lancer Docker
docker compose up -d

### 2 - Injecter les donnees
python inject_tweets.py
python inject_ventes.py

### 3 - Lancer le stream temps reel
python stream_realtime.py

### 4 - Lancer Spark NLP
docker cp spark_direct.py projet-sentiment-spark-1:/opt/spark/work-dir/
docker exec -it --user root projet-sentiment-spark-1 python3 /opt/spark/work-dir/spark_direct.py

### 5 - Lancer dbt
cd dbt_sentiment
dbt seed
dbt run

### 6 - Voir le dashboard
Ouvrir http://localhost:5601

## Technologies
- Apache NiFi : http://localhost:8080
- Elasticsearch : http://localhost:9200
- Kibana : http://localhost:5601
- Spark NLP : analyse de sentiment
- dbt : KPIs sentiment vs ventes

## Resultats
Baskets RunX    | Score: +0.82 | CA: 291,056 EUR | Sentiment tres positif
T-shirt Classic | Score: -0.67 | CA: 150,068 EUR | Sentiment tres negatif
