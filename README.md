﻿# Git-Tutorial

## Créer un projet avec GIT

Les personnalisations à la première installation

    git config --global core.editor "editeur"
    git config --global user.name "asfolken"
    git config --global user.email "email"
    
![File Statut](https://i.stack.imgur.com/ppgRW.png)

  1. Créer un projet, faire un commit, ajouter des fichiers dans le commit, voir les logs et les status
  
__git init__ -> créer un dossier géré par git     
__git add__ -> ajouter un ou plusieurs fichier dans le comit   
__git reset HEAD~1__ -> enlever un ou plusieurs fichier dans le comit ou revenir en arriere en local   
__git rm__ -> supprimer les fichiers et enlevé du staged 
__git mv from to__ -> deplacer les fichiers
__git status__ -> etat du commit et file status lifecycle      
__git commit -a -m "message"__ -> comité avec un message (-a permet de mettre tout les fichiers modifier dans le commit sans add)
__git commit --amend__ -> modifier le dernier comit    
__git log__ -> afficher les logs des différents commits     

    git init
    git add README.md
    git commit -m "first commit"
    git status
    git log
    
  2.  Envoyer, Télécharger les fichiers et vérifier les différences avec le repo   
  
__git remote -v__ -> voir les différents remotes du projet    
__git remote add origin__ -> lier notre projet git a un repository  
__git fetch origin__ ->  telecharger le remote
__git push -u remote branch__ -> uploader les fichiers dans le repository dans la branche master         
__git pull origin master__ -> télécharger les fichiers depuis le repository dans la branche master         
__git diff HEAD__ -> voir la différences des header entre ma version et le repo      
__git diff --staged__ ->  voir la différences au niveau des fichiers entre ma version et le repo       
    
    git remote add origin https://github.com/ASFolken/Git-Tutorial.git
    git push -u origin master
    git diff HEAD
    
  3. Gérer le système de branche  
  
__git branch branche_name__ -> créer une branche       
__git checkout branche_name__ ->  switcher d'une branche a une autre  (avec -b créer la branche et met le head dessus)
__git merge branche_name__ -> mélanger la branche avec le principal                      
__git rebase branche_name__ -> mélanger la branche avec le principal et retourne sur avancement linéaire    
__git branch -d branch name__ -> suprimer une branche
__git revert HEAD^__ -> revenir en arrière sur le remote
__git cherry-pick HEAD HEAD2__ -> copier le commit dans la branche actuelle
__git rebase -i HEAD__ -> rebase interactif
