# Veille Tech Automatisée avec n8n et Discord

Ce projet met en place un système de **veille technologique automatisée** utilisant **n8n**, des **flux RSS**, et un **webhook Discord**.

L'objectif est de récupérer automatiquement des informations récentes sur les technologies **IA, Data Engineering, MLOps et Cloud** et de les diffuser dans un salon Discord.

---

# Objectifs du projet

## Phase 1 — Veille RSS sans IA

Un workflow n8n lit plusieurs flux RSS provenant de blogs technologiques.

Les articles sont ensuite :

- fusionnés
- filtrés pour ne garder que ceux publiés dans les **24 dernières heures**
- formatés
- envoyés dans un salon Discord sous forme de **messages enrichis (Embeds)**

Le workflow s'exécute automatiquement chaque matin grâce à un **déclencheur horaire**.

---

## Phase 2 — Veille augmentée par IA

Un second workflow utilise un **LLM via OpenRouter** pour générer un **rapport de veille stratégique** sur les dernières actualités :

- Intelligence Artificielle
- Data Engineering
- MLOps
- Cloud

Le rapport généré est ensuite :

- parsé
- structuré
- envoyé dans Discord sous forme d'**Embeds classés par importance stratégique**.

---

# Lancer le projet

## Accéder au dossier docker

```
cd n8n-compose
```

## Lancer n8n avec Docker Compose
```
docker compose up -d
```
## L'interface n8n sera disponible à l'adresse
```
http://localhost:5678/
```

## Arrêter le projet

```
docker compose down
```