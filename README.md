
# Projet Docker

Nous avons donc besoin de créer 5 containers : 
* Un service “vote” pour l’interface de vote
* Une base Redis
* Une base postgres
* Un nommé “résultat” pour la gestion du résultat des votes
* Un worker pour faire le lien entre redis et postgres


Après avoir récupéré le repository du TP, voilà ce que nous avons fait :
> 1- Ecrire le fichier docker-compose.build.yml pour créer les images à utiliser
  lancement du traitement avec la commande : docker-compose -f docker-compose.build.yml build

> 2- Tagger les images déjà créer et les push dans le contener Registry pour utiliser nos propres images
   lancement du traitement avec les commandes :docker tag postgres:15-alpine localhost:5000/postgres:v0 et
   docker push localhost:5000/postgres:v0  (par exemple pour le container Postgres)
   et refaire ce traitement pour tous les autres containers

> 3- Ecrire le fichier compose.yml pour créer et lancer nos 5 containers
 lancement du traitement avec la commande : docker compose up -d


