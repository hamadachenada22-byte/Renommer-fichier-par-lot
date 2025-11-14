# Renommage des fichiers par lot 
## Groupe CEZAM
| Nom  |Prénom   | Numéro d'étudiant | 
|:-----|:-------:|------------------:|
|Fatima|OUHOCINE |20245633|
|Nada  |HAMADACHE|20246691|

## Dans le cadre de ce projet nous traitons le sujet de "Renommage de fichiers par lot". L’objectif est de concevoir un programme qui permet de renommer un grand nombre de fichiers en suivant un motif donné par l’utilisateur.
 ## Noyeau minimal:
 Le noyeau minimal peut comprter les fonctionnalités suivantes:
 ## #1 La définition des motifs de reconnaissances
 Permettre à l'utilisateur de selectionner et d'extraire les parties importantes dans un nom de fichiers via les éxpressions régulières.
 ## #2 La definition d'un schéma de renommage 
 Permet de spécifier la nouvelle forme de nom, en utilisant les parties extraites de la partie précédente.
 > cette étape dépend de #1.
 ## #3 Evitement des collisions
  Permet de vérifier qu’il n’existe pas des fichiers qui recevront le même nom de fichier après le renommage.
  > cette étape dépend de la partie #2.
  ## #4 La validation avant le renommage 
  Permet une correspondance entre les anciens et les nouveaux noms de fichiers afin de permettre à l’utilisateur de vérifier le résultat et de le confirmer avant son exécution réelle. Cette étape dépend des parties 2, 3, 4 et 5.
  > cette étape dépend des parties #1, #2, #3.
  ## #5 Exécution du renammage 
  c’est l’étape où on applique effectivement les modifications (les nouveaux noms aux fichiers).
  > cette étape dépend de la partie #5.
  # Fonctionnalités suuplémentaires:
  ## #6 La génération d’un script d’annulation 
  Permet de récupérer l’ancien nom pour chaque fichier (avant le renommage).  
  >Cette étape dépend de la partie #5.
  ## #7 Déplacement entre volumes
  Permet de déplacer les fichiers soit dans le même disque ou bien entre différents disques.
  >Cette étape dépend de la partie 5. 
  ## #8 La portabilité entre Windows, Linux et MacOs 
  Permet d’assurer le fonctionnement du programme sur Windows, Linux et MacOS. 
  >Cette étape dépend de la partie 5





