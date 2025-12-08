Renommage de fichier par lot 
----------------------------
Les Bibliothèques utilisées dans notre projet 
----------------------------------------------
1.shutil
Nous avons utilisé shutil pour déplacer les fichiers du dossier source vers le dossier destination.
La fonction shutil.move() nous a permis de renommer et déplacer les fichiers en même temps .

2.pathlib
Avec pathlib, nous avons pu manipuler les chemins de fichiers facilement.
Par exemple, créer des objets Path, parcourir les dossiers avec rglob("*") et vérifier si un fichier existe déjà.
Ça rend le code plus clair et compatible avec Windows, Linux ou Mac.

3.re
Nous avons utilisé re pour les expressions régulières, ce qui nous a permis de sélectionner seulement certains fichiers et de changer leurs noms automatiquement.
Par exemple, renommer tous les .jpeg en .png avec une seule ligne grâce à re.sub().

4.sys
La bibliothèque sys nous a servi à récupérer les arguments que l’utilisateur passe quand il lance le script dans le terminal.
Comme ça, nous pouvons choisir le dossier source, la regex, le nouveau nom et le dossier destination .

5.rich
Nous avons  utilisé rich pour que le script soit plus lisible et sympa à utiliser.
Avec Console et Table, nous affichons un tableau avec les anciens noms et les nouveaux noms pour que l’utilisateur puisse voir exactement ce qui va changer.
On peut même annuler si on n’est pas sûr, c’est pratique pour ne pas faire d’erreur.

Structure de code 
------------------
Script : essai10.py
├── Import des bibliothèques citées auparavant 
│  
│
├── Initialisation de la console Rich
│   └─ console = Console()
│
├── Fonction : afficher_fichiers(actions)
│   ├─ Paramètre : liste de tuples (ancien_nom, nouveau_nom)
│   ├─ Affiche un tableau avec les anciens et nouveaux noms
│   └─ Utilise rich.Table pour l’affichage
│
├── Fonction : renommer(dossier_source, regex, replacement, dossier_destination)
│   ├─ Convertit les chemins en objets Path
│   ├─ Crée le dossier de destination s'il n'existe pas
│   ├─ Recherche fichiers correspondant à la regex
│   ├─ Applique le renommage avec re.sub()
│   ├─ Gère les collisions de noms (_1, _2, etc.)
│   ├─ Affiche le tableau via afficher_fichiers()
│   ├─ Demande confirmation à l’utilisateur
│   └─ Déplace et renomme les fichiers avec shutil.move()
│
└── Bloc MAIN : if __name__ == "__main__"
    ├─ Vérifie que 4 arguments sont fournis : dossier_source, pattern, replacement, dossier_destination
    └─ Appelle la fonction renommer() avec ces arguments et exécute

Comment exécuter le script
--------------------------
Notre script prend 4 arguments sur la ligne de commande :
dossier_source : le dossier où se trouvent les fichiers à traiter.
pattern : l’expression régulière qui correspond aux fichiers que tu veux renommer.
replacement : le nouveau nom ou motif de remplacement pour les fichiers.
dossier_destination : le dossier où les fichiers renommés seront déplacés.

Exemple 1 : Renommer tous les .jpeg en .png et déplacer vers un autre dossier , avec la commande :

python essai10.py "C:/Users/Hamadache Nada/Pictures/Screenshots" "(.*)\.jpeg" "\1.png" "C:/tmp/photo/"

Exemple 2 : Renommer en ajoutant un préfixe IMG pour chaque fichier .png  

python essai10.py "C:/Users/Hamadache Nada/Pictures/Screenshots" "(.*)\.png" "IMG_\1.jpeg" "C:/tmp/photo/"

Répartion des taches :
------------------------

