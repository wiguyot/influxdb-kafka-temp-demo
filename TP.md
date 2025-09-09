# TP — Démo InfluxDB → Kafka (températures)

## Objectifs
- Pipeline minimal : **génération → InfluxDB → export Kafka**.
- Manipuler la requête/flux d’extraction vers Kafka.
- Valider le topic côté **consumer/Kafdrop**.

## Prérequis
- Docker + Docker Compose.
- Accès :
  - InfluxDB : `http://<HOST>:<INFLUXDB_HTTP_PORT>`  <!-- TODO -->
  - Broker : `<KAFKA_BROKER_HOST>:<KAFKA_BROKER_PORT>`  <!-- TODO -->
  - Kafdrop (option) : `http://<HOST>:<KAFDROP_PORT>`  <!-- TODO -->

## Démarrage rapide
```bash
git clone <ce dépôt>
cd influxdb-kafka-temp-demo
docker compose up -d
# (Option) Alimenter Influx
# python inject.py
```

## TP pas à pas

	1.	Injecter des données dans Influx (script ou API).

	2.	Vérifier le bucket et les mesures.

	3.	Exécuter l’export vers Kafka (script/Flux/Task du dépôt).

	4.	Consommer le topic cible ; valider schéma (clé/valeur).

	5.	Modifier la requête (champ/filtre/période) et observer l’effet.

## Critères de réussite

	•	Données dans Influx puis Kafka.

	•	Consommation en temps réel avec le format attendu.

	•	Mini note expliquant la transformation effectuée.

    