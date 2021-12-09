# big-data-project

Dans ce projet, il vous est demandé de réaliser une application en python qui récupérera en entrée les données issues d'un topic kafka et
les écrira dans un fichier csv après transformation et enrichissement.

## Prérequis et recommandations

Un environnement linux est recommandé pour pouvoir faire tourner l'ensemble des composants ainsi que developper et 
tester l'application dans les meilleurs conditions, il est néanmoins possible de le faire sous windows.

Dans tous les cas utiliser conda ou équivalent (venv ) pour créer votre environnement python 3.8.12 .

Ensuite installer et lancer [Kafka 3.0](https://kafka.apache.org/quickstart) (Pour windows suivre les mêmes instructions
indiquées mais en lançant les fichiers .bat au lieu de .sh contenus dans le répertoire bin/windows après extraction)

Pour spark deux options sont envisageables :

- Installer pyspark (3.2.0) et écrire votre code en se basant dessus.

- Installer un cluster spark en stand alone.

Ceci reste bien entendu un ensemble de recommandations et toute autre type de démarche est acceptable sous condition d'être documenté (via docker ou autre).

<b>Ce qu'il faut retenir en revanche sur la stack technique : </b>:

- Python = 3.8.12
- Kafka = 3.0.0
- Spark = 3.2.0

## Projet

On souhaite récupérer des données de vaccination fournies par différents centres situés partout en france en temps réél depuis kafka :

_département;vaccin;date;n_dose1;n_dose2;n_dose3;n_dose4_

avec pour colonnes :

**departement:** le département.   
**vaccin:** le type de vaccin administré.  
**date:** la date d'envoi/réception du decompte au format YYYY-MM-DD.  
**n_dose1:** nombre de gens ayants reçu une première injection de vaccin.  
**n_dose2:** nombre de gens ayants reçu une deuxième injection de vaccin.  
**n_dose3:** nombre de gens ayants reçu une troisième injection de vaccin.  
**n_dose4:** nombre de gens ayants reçu une quatrième injection de vaccin.

Exemple de ligne : 

```75;1;2021-12-10;1000;2000;1000;10```

avec pour les types de vaccins :

1 : COMIRNATY Pfizer/BioNTech
2 : Moderna
3 : AstraZeneka
4 : Janssen


Comme indiqué plus haut ce programme sera écrit en python en version 3.8 et devra utiliser spark et kafka.

[*hint*](https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html) 

## Questions

On suppose que le fichier vaccinations.csv soit un output à un instant t de notre programme ( en réalité c'est un fichier soigneusement importé et modifié depuis
[data.gouv](https://www.data.gouv.fr/fr/pages/donnees-coronavirus/).
En utilisant la liste des départements de France fournie également dans le dossier, répondre en justifiant (en utilisant spark et python  ) aux questions :

- Q1 : 
- Q2 : 
- Q3 :
- Q4 :
- Q5 :

## Notation
Algorithme : 7  
Outillage Kafka et Spark : 5    
Questions Spark SQL : 4   
Documentation et lisibilité : 3    
