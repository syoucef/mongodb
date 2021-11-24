# Utilisation de MongoDB
L'objectif dans ce qui suit est d'installer et d'importer des données dans le SGBD MongoDB, un système NoSQL orienté documents. On commence par télécharger la version community qui se trouve à l'adresse suivante : https://www.mongodb.com/try/download/community (version 3.2.22)

On lance les deux commandes suivantes ``mongod`` pour le serveur et ``mongo``pour le client. On commence par appréhender MongoDB, en utilisant le client ``mongo`` et puis utiliser un client graphique tel que ``Robo 3T``. 

Remarque  : le dossier de sauvegarde par défaut de MongoDB est ``/data/db``.  Si vous ne voullez pas utiliser ce répertoire mais un autre ``mongod --dpath $repetoiredesauvegarde``


Pour créer une base de donnée `use contacts`;

Pour créer une collection `db.createCollection("amis");` 

Pour créer une deuxième collection `db.cretaeCollection("profesionels")`;

Ajouter un document dans une collection `db.amis.insert({"prenom":"samir"})`; 

Il n'existe pas de schéma pour une base de données NoSQL en général. On peut donc insérer des éléments qui n'ont rien à voir les uns avec les autres. ``db.amis.insert({"numero":1234, "nom":"Alfred", "Tel":0665434343})``;

Le langage d'interoggartion d'une base de données MongoDB est propre à ce système et ne peut être utiliser pour interogger un autre de système de gestion de bases de données (contrairement à SQL). 

Pour afficher toutes les collections ``show collections;``  






Pour importer des données : ``$MONGO/bin/mongoimport --db my_db --collection restaurants $chemin/restaurants.json``







