# Projet-3-TRINITY
Application de trading 

Projet de Reconnaissance de Figures sur les Graphiques

Table des matières

Introduction
Architecture du Projet
Création de l'ETL avec Mage
Conteneurisation avec Docker
Collecte de Données avec AlphaVantage
Algorithme de Reconnaissance des Figures
Base de Données avec PostgreSQL ou MySQL
Notification et Visualisation
Conclusion
Introduction

Ce projet vise à détecter des motifs spécifiques sur les graphiques financiers en utilisant un pipeline ETL, des algorithmes de reconnaissance de figures et une interface utilisateur pour la visualisation et les notifications.

Architecture du Projet

Le projet comprend plusieurs composants :

API Data Collection : Collecte des données via l'API d'AlphaVantage.
Pipeline ETL : Extraction, transformation et chargement (ETL) des données.
Stockage des Données : Base de données relationnelle (PostgreSQL ou MySQL).
Reconnaissance des Figures : Algorithme de détection des motifs sur les graphiques.
Notification et Visualisation : Envoi de notifications et affichage des graphiques dans une interface utilisateur (application web ou mobile).
Orchestration avec Docker : Conteneurisation de tous les services.
Création de l'ETL avec Mage

Mage est une excellente solution pour construire un pipeline ETL. Voici les étapes :

Installation de Mage.
Configuration du pipeline :
Extraction : Collecte des données de marché via l'API AlphaVantage et stockage des données brutes.
Transformation : Nettoyage des données et ajout de calculs techniques.
Chargement : Insertion des données transformées dans PostgreSQL ou MySQL.
Automatisation des tâches récurrentes avec Mage.
Conteneurisation avec Docker

Chaque composant sera isolé dans son propre conteneur :

Utilisation de Docker Compose pour orchestrer les conteneurs nécessaires :
Un conteneur pour l'ETL Mage.
Un conteneur pour la base de données PostgreSQL/MySQL.
Un conteneur pour l'application de détection et de notification.
Un conteneur pour le serveur web (interface utilisateur).
Collecte de Données avec AlphaVantage

Inscription et obtention d'une clé API sur le site d’AlphaVantage.
Utilisation des points de terminaison de l’API pour obtenir les données en temps réel ou historiques.
Intégration des données dans le pipeline ETL via un script Python.
Algorithme de Reconnaissance des Figures

Prétraitement des données et création de graphiques en chandeliers.
Utilisation d'algorithmes de reconnaissance de motifs ou d'un modèle machine learning pour reconnaître des motifs spécifiques.
Configuration d'un service pour envoyer des notifications.
Base de Données avec PostgreSQL ou MySQL

Création de la base de données et définition des schémas nécessaires.
Configuration de la connexion entre Mage et la base de données pour le chargement des données.
Ajout d'index pour optimiser les requêtes de données.
Notification et Visualisation

Intégration d'un service de notifications comme Twilio, Firebase, ou des webhooks.
Création d'une interface utilisateur (web ou mobile) pour afficher les graphiques en temps réel.
Conclusion

Ce projet permet de détecter des motifs spécifiques sur les graphiques financiers et de notifier les utilisateurs en temps réel via une interface conviviale. Il repose sur un pipeline ETL robuste, des techniques de conteneurisation et des algorithmes de reconnaissance de figures.
