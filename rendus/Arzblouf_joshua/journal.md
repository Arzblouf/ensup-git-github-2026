# Carnet de bord

## Mes preuves

### Atelier 0
Récupération du projet avec fork et création du clone.

### TP1
-> add prépare les modifications dans l'index pour le prochain commit.
-> Il manquera la phrase "Inscription sur place", ajouté après la commande add
-> L'index est la zone de préparation du prochain commit, il ne contiens donc que les modifications ajoutées avec la commande add, un fichier enregistré n’est donc pas automatiquement ajouté à l'index.
Différence : Le fichier enregistré est dans le dossier de travail alors que l'index contient ce qui est préparé (pour le commit)

### Enquête 1
Création du fichier acces.md.

Prédiction : git diff n’affichera pas le fichier car il n'est pas suivi.
Observations :
    git status --short -> ?? acces.md
    git diff -> rien
    git add acces.md -> le fichier passe dans l’index
    git diff --cached -> le fichier apparait
Explication :
    Git diff compare le dossier de travail à l'index pour les fichiers suivis uniquement. Un fichier non suivi n'apparaît pas avec git diff car il n'est pas dans l'index.
Preuve :
    Commit retrouvé par -> git show (qui m'affiche le dernier commit)

### TP 2
Prédiction main : programme.md sera absent car le commit n'existe que sur la branche feature/programme
-> Après la fusion, le fichier est présent.
-> Il faut être sur la branche main pour intégrer une évolution dans main et la commande "git log --oneline" permet de vérifier le contenu et sa branche d'origine.

### Enquête 2
-> Lors que l'on modifie un fichier sur une branche différente, il n'y a pas de conflit pendant le merge car les 2 fichiers sont différents. Il y aurait eut un conflit de versions si le même fichier était modifié dans 2 branches différentes avant le merge.
-> Les deux parents sont main et feature/accessibilite

### TP 3
-> git remote -v : origine est bien Arzblouf (mon compte). 
URL PR : https://github.com/AbidHamza/ensup-git-github-2026/pull/2
Différence : un fork est une copie d'un dépôt Github sur mon compte, un clone est une copie d'un dépôt sur mon pc et une branche est une ligne de développement à l'intérieur d'un dépôt

### Enquête 3
-> Permission denied : connexion avec un autre compte : vérifierque git remote -v montre son pseudo
-> non-fast-forward : github contient des commits que je n'ai pas sur ma machine (commit en ligne par exemple) : utiliser git fetch origin pour récupérer sans fusionner puis git merge origin main
-> nothing to commit : fichier non enregistré, ignoré ou mauvais dossier : vérifier que l'éditeur ai bien enregistré les modifications, git check-ignore pour vérifié s'il est ignoré ou ls pour vérifier qu'il s'agit du bon fichier

### TP 4
URL de la PR : https://github.com/Arzblouf/ensup-git-github-2026/pull/1