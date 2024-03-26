
Ce projet vise à automatiser le processus d'extraction d'informations à partir de factures en utilisant des techniques de Traitement du Langage Naturel (NLP).

`Description`
Le code fourni ici utilise plusieurs bibliothèques Python pour extraire des informations à partir d'une image de facture et PDF. Voici un aperçu de ce que le code accomplit :

`Extraction de texte de l'image PDF :`
L'image du PDF est ouverte et le texte est extrait en utilisant Tesseract OCR.
Extraction des articles de la facture :
Les informations sur les articles, telles que la description, la quantité, le prix unitaire, etc., sont extraites à l'aide d'expressions régulières.

`Traitement sémantique avec spaCy :`
Des informations spécifiques telles que le numéro de facture sont extraites à l'aide d'expressions régulières.
L'analyse sémantique est effectuée à l'aide de spaCy pour extraire des entités nommées comme les noms de vendeur et de client.

