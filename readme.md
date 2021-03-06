# TP Programmation Serveur - Composants

Développement d'une application de gestion d'annuaire en s'appuyant sur SpringBoot, Kafka
et Docker.

## Environnement de développement

### Pré-requis

* JDK 1.8
* Composer
* Docker
* Docker-compose
* Kafka 2.10-0.10

### Technologies

* Spring-boot
* Angular
* Thymeleaf
* HSQLDB
* nodejs 16
* npm 8.1.2

### Lancer l'environnement de développement

Toutes les commandes sont réalisées sous Windows.

### Récupération du dépôt github
```
git clone https://github.com/Yann-Malaquin/Annuaire.git
```

### Lancement du container Docker
```bash
docker-compose up --build
```

## Kafka

### Utilisation Kafka

Nom du topic : annuaire<br/>
Format Json :

```json 
{"name": "Hood","surname": "Shannon","phone": "+33 (816) 462-3396","city": "Johnsonburg"}
```

Un fichier est également fourni pour avec plusieurs personnes. <br/>
Nom du fichier : producer.json


Pour accéder à Kafka, ouvrir un terminal, saisir la commande suivante

Pour envoyer des données en CMD
```bash
docker exec -ti annuaire-kafka /bin/sh
```

```shell
sh-4.4$ kafka-console-producer --broker-list kafka:9092 --topic annuaire
> {"name": "Hood","surname": "Shannon","phone": "+33 (816) 462-3396","city": "Johnsonburg"}
```

Appuyez sur entrée. <br/> 
Rafraîchir la page web et si le modèle correspond, la personne sera ajoutée.

## URL

#### Thymeleaf

- Affichage de toutes les personnes : [localhost:8082/annuaire](http://localhost:8082/annuaire)
- Ajout d'une personne [localhost:8082/annuaire/addPerson](http://localhost:8082/annuaire/addPerson)

#### Angular

- Page d'accueil : [localhost:4200/](http://localhost:4200/)

Ensuite utilisation de la navbar pour naviguer au travers de l'application.

## Postman

TP Annuaire.postman_collection
