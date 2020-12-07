# Semaine d'introduction
## Semaine 1 - Semaine d'introduction au code -> Mehdi
## Semaine 2 - Introduction au Code           -> Rémi
## GIT 


* Initialiser un répo git en local :
```language-shell 
$ git init
```
* Ajouter nom_fichier à ton futur commit :
```language-shell 
$ git add nom_fichier
```
* Faire un commit avec pour message message_commit :
```language-shell 
$ git commit -m "message_commit"
```

* Afficher l'état de tes fichiers par rapport au commit que tu es en train de réaliser (⚠ commande très pratique, à faire tout le temps) :
```language-shell 
$ git status
```

* Afficher les modifications de nom_fichier entre le dernier commit et le fichier actuel :
```language-shell 
$ git diff nom_fichier
```

* Afficher l'historique des commits :
```language-shell 
$ git log
```

* Revenir en mode lecture uniquement au commit SHA :
```language-shell 
$ git checkout SHA
```

* Revenir au commit actuel :
```language-shell 
$ git checkout master
```

* Tout effacer pour revenir au commit SHA :
```language-shell 
$ git reset --hard SHA
```

* Tout effacer pour revenir au dernier commit :
```language-shell 
$ git reset --hard
```

* Sauvegarder provisoirement son travail sans le commit :
```language-shell 
$ git stash
```

* Récupérer un travail précédemment sauvegardé avec `git stash` :
```language-shell 
$ git stash pop
```

* Voir les différentes remotes de ton repo git :
```language-shell 
$ git remote -v
```

* Ajouter la remote url_remote à la liste de tes remotes. Cette remote aura le nom nom_remote (par convention, la remote principale où il y a le code s'appelle origin) :
```language-shell 
$ git remote add nom_remote url_remote
```

* Pousser ta branche nom_branche vers ta remote nom_remote :
```language-shell 
$ git push nom_remote nom_branche
```

* Récupérer ta branche nom_branche de ta remote nom_remote :
```language-shell 
$ git pull nom_remote nom_branche
```



## Semaine 3 - Découverte de Ruby             -> Mehdi

# Fullstack web
## Semaine 1 - Programmation Orientée Objet   -> Rémi
## Semaine 2 - Initiation à Rails             -> Mehdi
## Semaine 3 - Rails intermédiaire            -> Rémi
## Semaine 4 - Rails avancé                   -> Mehdi
## Semaine 5 - HTML / CSS                     -> Rémi
## Semaine 6 - JavaScript de front            -> Mehdi
## Semaine 7 - Projet : boutique en ligne
## Semaine 8 - Projet Final 1
## Semaine 9 - Projet Final 2