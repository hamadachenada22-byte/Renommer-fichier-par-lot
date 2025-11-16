# Rendu 2 : identification des briques logicielles utilisables.
## Les briques logicielles pour le moyeau minimal.
### Fonctionalité #1: La définition des motifs de reconnaissances.
 * Modules python standard (re)
   * Service rendu: permet de définir et exécuter des expressions régulières pour extraire des motifs dans les noms de fichiers.
   * Limites : certaines regex très avancées ne sont pas supportées.
   * Installation : aucune (standard).
   * Facilité d’utilisation : syntaxe simple.
   * Compatibilité : ça marche sur Windows, Linux et Mac.
   * Maintenance : très bonne.
   * Documentation : excellente.
 * Bibliothèques tierces(regex).
   * service rendu: version plus avancée de re, avec des fonctionnalités supplémentaires.
   * Limites : dépendance externe, API un peu plus lourde.
   * Installation:  pip install regex ( mais facile à installer).
   * Compatabilité : très bonne.
   * decumentation: bonne .
  ----------------------------------------------------------------------------------------
  ### Fonctionnalité #2: La definition d'un schéma de renommage.
  * Bibliothèque standard (f-strings / str.format()).
    * Service rendu: permet de construire facilement un nouveau nom de fichier en combinant des morceaux extraits.
    * Limites : aucune validation automatique du schéma.
    * Installation : aucune.
    * Utilisation : simple et intuitive.
    * Documentation : bonne.
  * string.template
    * Service rendu : propose une manière simple d’écrire un modèle (${nom}, ${date}…).
    * Limites : moins puissant que les f-strings.
    * Installation : aucune.
    * Utilisation : facile.
    * Documentation : bonne.
  ----------------------------------------------------------------------------------------
 ### Fonctionalité #3: Evitement des collisions:
 * Bibliothèque standard : os.path.exists / pathlib.Path.exists.
   * Service rendu : permet de vérifier si un fichier existe déjà pour éviter d’écraser un fichier existant.
   * Limites : ne génère pas automatiquement un nom alternatif.
   * Installation : aucune.
   * Utilisation : simple.
   * Compatibilité : ça marche sur windows, linux et MacOs.
 * Bibliothèques tierces: (python-slugify)
   * Service rendu : permet de “nettoyer” les noms (supprimer accents, espaces…).
   * Limites : ne gère pas les collisions tout seul.
   * Installation : pip install python-slugify.
   * Utilisation : facile.
   * Documentation / communauté : bonne.
  ----------------------------------------------------------------------------------------
  ### Fonctionlité #4 : validation avant renommage:
 * tabulate.
   * Service rendu : permet d’afficher facilement un tableau avec les anciens et nouveaux noms.
   * Limites : nécessite installation.
   * Installation : pip install tabulate.
   * Utilisation : simple.
   * Documentation : bonne.
 * rich.
   * Service rendu : permet des tableaux et affichages plus jolis dans le terminal.
   * Limites : bibliothèque plus lourde.
   * Installation : pip install rich.
   * Utilisation : simple.
   * Documentation : bonne.
  ----------------------------------------------------------------------------------------
  ### Fonctionnalité #5 : Exécution de renommage.
   * Bibliothèque standard (os.rename):
     * service rendu: renomme un fichier.
     * Limites : comportement différent selon les OS si le fichier cible existe déjà.
     * Installation : aucune.
   * Bibliothèques tierces (sutil.move).
     * Service rendu : renomme ou déplace un fichier.
     * Limites : un peu plus lent, mais plus fiable.
     * Installation : aucune.
     * Compatibilité : très bonne.
  ----------------------------------------------------------------------------------------
## Les briques logicielles pour les fonctionnalités supplémentaires:
 ### fonctionnalité #6: La génération d'un script d'annulation.
 * Bibliothèque standard(csv).
   * Service rendu : stocker la correspondance (ancien nom → nouveau nom) pour pouvoir restaurer ensuite.
   * Limites : ne crée pas un script automatique.
   * Facilité d’utilisation : bonne.
   * Installation:aucune.
  ----------------------------------------------------------------------------------------
  ### Fonctionnalité #7: Déplacement entre volume .

* Bibliothèque standard(shutil.move).
  * Service rendu : gère les déplacements entre répertoires et même entre disques différents.
  * Limites : peut être lent sur de gros fichiers.
  * Installation:aucune.
* Bibliothèques tierces (rsync, robocopy)
  * Service rendu : déplacement très rapide et fiable.
  * Limites : pas portable (dépend du système).
  * Installation : parfois nécessaire.

------------------------------------------------------------------------------------------
### Fonctionnalité #8: Portabilité entre Windows , linux et MacOs.
 * Bibliothèque standard (pathlib).
   * Service rendu : gère automatiquement les chemins en fonction du système.
   * Limites : très peu.
   * Installation : aucune.
   * Documentation : excellente.
 * Docker
   * Service rendu : permet de créer un environnement identique sur tous les OS.
   * Limites : installation lourde, peut être trop pour ce projet.
