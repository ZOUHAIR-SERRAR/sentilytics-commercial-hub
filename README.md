# sentilytics-commercial-hub
Contexte :Une marque veut corréler les mentions Twitter/Instagram avec les ventes. 

Objectifs:StreamerlestweetsviaTwitterAPIv2,extrairelessentimentsavecunmodèle BERT fine-tuné (ou camembert), joindre aux transactions, produire des KPIs (sentiment score vs chiffre d’affaires) dans un dashboard temps différé.

Technologies : Apache NiFi, Spark NLP, Elasticsearch, Kibana, dbt.
Aspects avancés : Analyse d’aspects (aspect-based sentiment), détection de campagnes
virables.
