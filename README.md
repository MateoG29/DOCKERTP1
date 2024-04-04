# DOCKERTP1
Création d’une application monitorée avec Docker


# Docker Flask Prometheus Grafana Project

Ce projet vous permet de déployer une application Flask, Prometheus et Grafana à l'aide de Docker.

## Contenu

1. [Introduction](#introduction)
2. [Prérequis](#prérequis)
3. [application-flask](#Application_Flask)
4. [Utilisation](#utilisation)
5. [Configuration](#configuration)
6. [Contributions](#contributions)
7. [Licence](#licence)

## Introduction

Ce projet permet de créer avec Docker, une application Flask, de récupérer les metrics avec Prometheus et les mettre en forme via Grafana.

## Prérequis

Avant de commencer, assurez-vous d'avoir docker sur votre machine.

## Application Flask

1. Créer un répertoire Docker dans lequel vous pourrez mettre vos fichiers.
2. Récupérer le fichier app.py, fichier dans lequel se trouve l'application Flask.
3. Récupérer le fichier requirements.txt pour les dépendances de l'application.
4. Récupérer le dockerfile qui permettra de construire l'image de l'application.

#Construire l'image de l'application : sudo docker build -t app Docker

