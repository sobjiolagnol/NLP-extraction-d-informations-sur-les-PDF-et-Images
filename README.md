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
