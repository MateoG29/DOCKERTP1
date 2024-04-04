# DOCKERTP1
Création d’une application monitorée avec Docker


# Docker Flask Prometheus Grafana Project

Ce projet vous permet de déployer une application Flask, Prometheus et Grafana à l'aide de Docker.

## Contenu

1. [Introduction](#introduction)
2. [Prérequis](#prérequis)
3. [Application Flask](#application-flask)
4. [Docker Compose](#docker-compose)
5. [Configuration](#configuration)

## Introduction

Ce projet permet de créer avec Docker, une application Flask, de récupérer les metrics avec Prometheus et les mettre en forme via Grafana.

## Prérequis

Avant de commencer, assurez-vous d'avoir docker sur votre machine.

## Application Flask

1. Créer un répertoire Docker dans lequel vous pourrez mettre vos fichiers.
2. Récupérer le fichier app.py, fichier dans lequel se trouve l'application Flask.
3. Récupérer le fichier requirements.txt pour les dépendances de l'application.
4. Récupérer le dockerfile qui permettra de construire l'image de l'application.

### Construire l'image de l'application : 
```sudo docker build -t app Docker```

### Pour vérifier que l'image a bien été créée :
```sudo docker images```

## Docker Compose
Pour créer les différents conteneurs, il vous faudra d'abord récupérer les fichiers prometheus.yml ainsi que docker-compose.yml.

### Démarrer les conteneurs
```sudo docker-compose up -d```
### Vérifier leur fonctionnement 
```sudo docker ps -a```

### Test
Si vos conteneurs sont bien UP vous pouvez alors vous connecter sur les différentes applications 
- Flask : ```http://votreip:5000```
- Grafana : ```http://votreip:3000```
- Prometheus : ```http://votreip:9090```

## Configuration
### Pour Prometheus
Aller dans Targets et vérifier qu'elles sont UP
### Pour Grafana
1. Aller dans Connections -> Data sources -> Add Data sources
2. Ajouter prometheus
3. Entrer l'url ```http://nomduservice:9090```
4. Save & Test
5. Aller dans Dashboards -> Add Visualization -> Prometheus
6. Dans Metric entrer flask_http_request_total -> Run queries
7. Sauvegarder votre Dashboard
