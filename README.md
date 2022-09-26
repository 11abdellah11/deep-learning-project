# deep-learning-project



# Détection du visage à l’aide de Tensorflow object detection

![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.001.png)

Etapes du code :

**Etape 1** :

Créer le dossier : Projet à tensorflow\_object\_detectionàdossier [ nom du nouveau en vironnement] se crée à l’aide de la commande :

python -m venv [nom de l’envoronnement :myprojet]

Activer ensuite l’envirronnement :

` `>.\ [nom de l’envoronnement  \Scripts\activate # Windows 

Ensuite installer  les dependaces et ajouter l’environnement à Python Kernel :

python -m pip install --upgrade pip

pip install ipykernel

python -m ipykernel install --user --name=tfodj

- Déposer le fichier du script dans le dossier tensorflow\_object\_detection
- Sur CMD en administrateur faut taper :> jupyter notebook 
- Choisir le nom de domaine d’environnement virtuelle et faut être sûr que vous êtes  dans le bon domaine.

**Etape 2 :**

- Exécuter le code 
- Une fenêtre du programme labellmg va apparaitre ouvrir le dossier dataimages et commencer le cadrage des images
- Construire deux dossier Train(qui va contenir les images et leurs annotations et qui sert à entrainer le modèle choisi) et Test va contenir des images pour évaluer le modèle choisis.
- Déposer ces deux dossiers dans …/workspae /images .

![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.002.png)

Pour vérifier l’installation du programme de  Tensorflow object\_detection il faut obtenir le message suivant

![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.003.png)

Il faut absolument cliquer sur Restart dans la case « cell »  car la comande import object\_detection pose une erreur








**Entrainement du modèle et évaluation :**

![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.004.png)

![Une image contenant texte, clavier, tableau de points

Description générée automatiquement](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.005.png)

Choisir un modèle sur : https://github.com/tensorflow/models/blob/master/research/object\_detection/g3doc/tf2\_detection\_zoo.md

Pour évaluer les métriques : on peut aller sur tensorboard en exécutant la commande suivante :![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.006.png)

On peux visualiser mAP ( :mean average precision) et Recall sur tensorboard![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.007.png) ![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.008.png)



![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.009.png)![](Aspose.Words.15b1373d-e76b-4550-82ef-a1c351350fe0.010.png)

Anonymisation :** 

Afin d’anonymiser le visage on peut procéder avec deux méthode différentes, la première consiste à superposer un masque défini par les 4 points issus de la prédiction du modèle (xmin,xmax,ymin,ymax). La deuxième méthode c’est d’appliquer un random sur toute les pixels contenus dans le box de prédiction.




