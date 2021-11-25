# Interrogation de MongoDB
L'objectif dans ce qui suit est d'installer et d'importer des données dans le SGBD MongoDB, un système NoSQL orienté documents. On commence par télécharger la version community qui se trouve à l'adresse suivante : https://www.mongodb.com/try/download/community (version 3.2.22)

On lance les deux commandes suivantes ``mongod`` pour le serveur et ``mongo``pour le client. On commence par appréhender MongoDB, en utilisant le client ``mongo`` et puis utiliser un client graphique tel que ``Robo 3T``. 

Remarque  : le dossier de sauvegarde des bases de données par défaut de MongoDB est ``/data/db``.  Si vous ne voullez pas utiliser ce répertoire mais un autre ``mongod --dpath $repetoiredesauvegarde``. Le port d'écoute par défaut de MongoDB est ``27017``. 


Pour créer une base de donnée `use contacts`; (on utilise un intérpreteur Javascript). 

Pour créer une collection `db.createCollection("amis");` 

Pour créer une deuxième collection `db.cretaeCollection("profesionels")`;

Ajouter un document dans une collection `db.amis.insert({"prenom":"samir"})`; 

Il n'existe pas de schéma pour une base de données NoSQL en général. On peut donc insérer des éléments qui n'ont rien à voir les uns avec les autres. ``db.amis.insert({"numero":1234, "nom":"Alfred", "Tel":0665434343})``;

Le langage d'interoggartion d'une base de données MongoDB est propre à ce système et ne peut être utiliser pour interogger un autre de système de gestion de bases de données (contrairement à SQL). 

Pour afficher toutes les collections ``show collections;``

Pour afficher tous les documents ``db.amis.find();``  

``{ "_id" : ObjectId("619e30bbf168d42f513793ae"), "nom" : "Youcef", "telephone" : 14112994 }``MongoDB attribué un identifiant unique pour chaque document. On peut nous-mêmes donner un identifiant que l'on veut insérer ``db.amis.insert({"_id":1, "nom":"samuel", "Tel":065454321});``.  


Pour parcourir toute une collection : ``db.films.find();``

Pour compter le nombre d'éléments d'une collection ``db.films.find();``

Pour afficher les 15 éléments d'une collection à partir du 11 ème élément ``db.amis.find().skip(1).limit(12)`` 

Pour trier une collection ``db.films.find().sort({"nom":1})`` La valeur 1 est pour le tri décroissant et -1 pour un tri croissant. 

Pour chercher un élément sachant son identifiant ``db.amis.find({"_id":1})``

On peut faire une recherche en utilisant des motifs plus complexe ``db.amis.find({"nom":"Youcef", "telephone":14112994})``




Télécharger le document json des restaurants de New-York. 

Pour importer des données dans MongoDB : ``$MONGO/bin/mongoimport --db mabase --collection restaurants $chemin/restaurants.json``. ``mabase``est le nom de votre base de données, et ``restaurants``est le nom de votre collection. 



#### Filtrage et projection avec un motif JSON


#### Création d'une séquence d'opérations

#### Mise à jour des données



# Protéger vos données grâce au ReplicaSet

Pour instancier une Replicaset, par exemple composé de trois serveurs (un ``Primary`` et deux ``Secondary``), il faut définir :

1. Un répertoire de stockage pour chaque serveur ;
2. Lancer chacun des serveurs 




# Distribuer vos données avec MongoDB


# Travail à rendre : 


#### Exercice 

Développer un micro-service qui utilise pour la persistance des données MongoDB. Créer une image Docker de votre service et renseigner le lien au début (vraiment au début) de votre redme.md pour la télécharger.  










