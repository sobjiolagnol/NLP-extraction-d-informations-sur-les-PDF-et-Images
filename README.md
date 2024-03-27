# **1) Projet d'analyse d'une facture**

Ce projet vise à automatiser le processus d'extraction d'informations à partir de factures en utilisant des techniques de Traitement du Langage Naturel (NLP) pour répondre à des questions de l'utilisateur.
Ici nous utilisons deux approches.

    1) L'approche tradictionnelle
    2) Un modèle pré-entrainé 

# Questions:

    1) how many invoice items are listed?
    2) what's the tax ratio applied?
    3)  can you give the sum of the growth worth of the two fist items?


# Description
       
Le code fourni extrait des informations à partir d'une image de facture et de fichiers PDF en utilisant Tesseract OCR pour le texte, des expressions régulières pour les articles de facturation, et spaCy pour l'analyse sémantique afin d'extraire des entités telles que les descriptions, la quantité,..etc. et mettre un modèle sur pieds pour repondre à certaines questions.



# **2) Extractions des données dans les fichiers PDF**

     L'objectif est d'extraire des informations de plusieurs documents PDF et de les rendre prêtes à être utilisées.


# 3) Job Salary Prediction

Ce projet consiste à prédire les salaires des offres d'emploi en se basant sur différentes caractéristiques extraites des annonces d'emploi. Le jeu de données utilisé provient de Kaggle et comprend un grand nombre de lignes représentant des annonces d'emploi individuelles, ainsi qu'une série de champs sur chaque annonce d'emploi.

## Description des champs

* `Id` - Identifiant unique pour chaque annonce d'emploi.
* `Title` - Champ de texte libre fourni par l'annonceur de l'emploi comme titre de l'annonce d'emploi.
* `FullDescription` - Le texte complet de l'annonce d'emploi tel que fourni par l'annonceur de l'emploi.
* `LocationRaw` - Lieu en texte libre tel que fourni par l'annonceur de l'emploi.
* `LocationNormalized` - Lieu normalisé par Adzuna à partir de notre propre arbre de localisation.
* `ContractType` - Temps plein ou temps partiel, interprété par Adzuna à partir de la description ou d'un champ supplémentaire spécifique reçu de l'annonceur.
* `ContractTime` - Permanent ou contrat, interprété par Adzuna à partir de la description ou d'un champ supplémentaire spécifique reçu de l'annonceur.
* `Company` - Nom de l'employeur tel que fourni par l'annonceur de l'emploi.
* `Category` - Catégorie de l'emploi parmi 30 catégories standard, déduite de manière assez confuse en fonction de la source de l'annonce.
* `SalaryRaw` - Champ de salaire en texte libre reçu dans l'annonce d'emploi de l'annonceur.
* `SalaryNormalised` - Salaire annuel interprété par Adzuna à partir du salaire brut.
* `SourceName` - Nom du site Web ou de l'annonceur à partir duquel nous avons reçu l'annonce d'emploi.

Toutes les données sont réelles, provenant d'annonces d'emploi en direct, et sont donc clairement sujettes à beaucoup de bruit du monde réel, y compris, mais sans s'y limiter : annonces qui ne sont pas basées au Royaume-Uni, salaires incorrectement déclarés, champs incorrectement normalisés et annonces dupliquées.

## Tâches

* Afficher la distribution de la variable cible (`SalaryNormalized`).
* Calculer le salaire moyen pour chaque catégorie d'emploi (`Category`) et trier les résultats par ordre décroissant. Quelle catégorie correspond au salaire moyen le plus élevé ?
* Appliquer une transformation logarithmique à la variable cible et afficher la distribution de la nouvelle variable. Utiliser la nouvelle variable comme cible.
* Explorer la description du poste (`FullDescription`), puis effectuer un prétraitement et une vectorisation à l'aide de la méthode `TF-IDF`.
* Diviser les données en conservant 20 % pour les tests. N'oubliez pas de fixer l'état aléatoire.
* Utiliser une régression Ridge en ne prenant en compte que les caractéristiques extraites des descriptions de poste. Évaluer le modèle avec la métrique $R^2$ sur les données d'entraînement et de test.
* Vérifier le modèle en utilisant les tests suivants :
* `'Directeur'`,
* `'Manager'`,
* `'Data Scientist'`,
*  `'Data Engineer'`,
*  `'Machine Learning Engineer'`.
* Afficher les 10 caractéristiques avec les poids positifs les plus élevés et les 10 caractéristiques avec les poids négatifs les plus élevés.
* Essayer différentes valeurs d'hyperparamètres :
    * Algorithmes `Ridge`/`Lasso` : paramètre de régularisation.
    * `TfIdfVectorizer`/`CountVectorizer` et certains de leurs paramètres.
* Essayer de combiner les caractéristiques textuelles avec d'autres caractéristiques du jeu de données source.
