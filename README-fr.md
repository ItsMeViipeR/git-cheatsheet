# Git Cheatsheet

# Table des matières

- [Git Cheatsheet](#git-cheatsheet)
- [Commandes](#commandes)
- [Exemples](#exemples)

# Commandes

| Commande                   | Description                                               |
| -------------------------- | --------------------------------------------------------- |
| `git init`                 | Initialiser un nouveau dépôt Git                          |
| `git clone <url>`          | Cloner un dépôt                                           |
| `git status`               | Afficher l'état de l'arborescence de travail              |
| `git add`                  | Ajouter des fichiers à la zone de staging                 |
| `git commit`               | Enregistrer les modifications dans le dépôt               |
| `git push`                 | Envoyer les modifications au dépôt distant                |
| `git pull`                 | Récupérer et fusionner les modifications du dépôt distant |
| `git checkout <branch>`    | Passer à une branche                                      |
| `git checkout -b <branch>` | Créer une nouvelle branche                                |
| `git merge <branch>`       | Fusionner une branche dans la branche actuelle            |
| `git branch`               | Lister toutes les branches                                |
| `git branch -d <branch>`   | Supprimer une branche                                     |
| `git log`                  | Afficher l'historique des commits                         |
| `git reset <file>`         | Désindexer un fichier                                     |
| `git revert <commit>`      | Revenir à un commit spécifique                            |
| `git stash`                | Mettre de côté les modifications                          |
| `git stash pop`            | Appliquer les modifications mises de côté                 |
| `git remote -v`            | Afficher les dépôts distants                              |
| `git fetch`                | Récupérer les modifications du dépôt distant              |

# Exemples

## Initialisation d'un dépôt :

```bash
git init
```

Cette commande crée un dossier `.git` contenant toutes les informations sur votre dépôt (branches, commits, etc.).

## Clonage d'un dépôt

```bash
git clone https://github.com/ItsMeViipeR/git-cheatsheet
```

Cette commande crée un nouveau dossier (ici `git-cheatsheet`) dans votre répertoire de travail (sous UNIX, vous pouvez voir le chemin avec la commande `pwd`).

Pour commencer à modifier, allez dans ce dossier, faites vos modifications et utilisez [`git commit`](#enregistrement-des-modifications) et [`git push`](#envoi-des-modifications).

## État du dépôt

L'état du dépôt contient les informations sur les fichiers suivis par Git (fichiers ajoutés, modifiés, supprimés, etc.).

```bash
git status
```

## Ajouter un fichier à un dépôt Git

Pour ajouter un fichier à la zone de staging dans votre dépôt Git, utilisez la commande `git add` suivie du nom du fichier. Par exemple, pour ajouter un fichier nommé `example.txt`, exécutez :

```bash
git add example.txt
```

Cette commande indique à Git de commencer à suivre les modifications du fichier spécifié et le prépare pour le prochain commit. Vous pouvez également utiliser `git add .` pour ajouter toutes les modifications dans le répertoire courant.

## Enregistrement des modifications

Pour enregistrer les modifications dans votre dépôt Git, utilisez la commande `git commit` suivie de l'option `-m` et d'un message décrivant les modifications. Par exemple :

```bash
git commit -m "Ajout de example.txt avec contenu initial"
```

Cette commande crée un nouveau commit dans le dépôt avec les modifications mises en staging et associe un message descriptif. Le message de commit doit être concis mais explicite, résumant l'objectif des modifications.

## Envoi des modifications

Pour envoyer les modifications à un dépôt distant, utilisez la commande `git push` suivie du nom du dépôt distant (généralement `origin`) et du nom de la branche. Par exemple, pour envoyer les modifications de la branche `main`, exécutez :

```bash
git push origin main
```

Cette commande télécharge vos commits locaux sur la branche spécifiée du dépôt distant. Assurez-vous d'avoir les permissions nécessaires et que votre branche est à jour avec la branche distante pour éviter les conflits.

## Récupération des modifications

Pour récupérer les modifications d'un dépôt distant et les fusionner dans votre branche actuelle, utilisez la commande `git pull` suivie du nom du dépôt distant (généralement `origin`) et du nom de la branche. Par exemple, pour récupérer les modifications de la branche `main`, exécutez :

```bash
git pull origin main
```

Cette commande récupère les dernières modifications de la branche spécifiée du dépôt distant et les fusionne dans votre branche locale. Elle combine les commandes `git fetch` et `git merge`. Assurez-vous que votre branche locale est à jour et sans conflits avant de récupérer les modifications.

## Changer de branche

Pour passer à une branche existante dans votre dépôt Git, utilisez la commande `git checkout` suivie du nom de la branche. Par exemple :

```bash
git checkout feature-branch
```

Cette commande met à jour votre répertoire de travail pour correspondre à la branche spécifiée.

## Création d'une nouvelle branche

Pour créer et passer à une nouvelle branche, utilisez la commande `git checkout -b` suivie du nom de la branche. Par exemple :

```bash
git checkout -b new-feature
```

Cette commande crée une nouvelle branche nommée `new-feature` et y passe.

## Fusion de branches

Pour fusionner une branche dans votre branche actuelle, utilisez la commande `git merge` suivie du nom de la branche. Par exemple :

```bash
git merge feature-branch
```

Cette commande intègre les modifications de `feature-branch` dans votre branche actuelle.

## Lister les branches

Pour lister toutes les branches de votre dépôt, utilisez la commande `git branch` :

```bash
git branch
```

Cette commande affiche une liste de toutes les branches, avec la branche actuelle mise en évidence.

## Suppression d'une branche

Pour supprimer une branche, utilisez la commande `git branch -d` suivie du nom de la branche. Par exemple :

```bash
git branch -d old-feature
```

Cette commande supprime la branche nommée `old-feature`.

## Affichage de l'historique des commits

Pour afficher l'historique des commits de votre dépôt, utilisez la commande `git log` :

```bash
git log
```

Cette commande affiche une liste des commits, incluant leurs hash, auteurs, dates et messages.

## Désindexation d'un fichier

Pour désindexer un fichier ajouté à la zone de staging, utilisez la commande `git reset` suivie du nom du fichier. Par exemple :

```bash
git reset example.txt
```

Cette commande retire le fichier de la zone de staging mais conserve les modifications dans votre répertoire de travail.

## Revenir à un commit

Pour revenir à un commit spécifique, utilisez la commande `git revert` suivie du hash du commit. Par exemple :

```bash
git revert abc1234
```

Cette commande crée un nouveau commit qui annule les modifications introduites par le commit spécifié.

## Mise de côté des modifications

Pour sauvegarder temporairement vos modifications sans les enregistrer, utilisez la commande `git stash` :

```bash
git stash
```

Cette commande sauvegarde vos modifications et rétablit votre répertoire de travail à l'état du dernier commit.

## Application des modifications mises de côté

Pour appliquer les modifications mises de côté les plus récentes, utilisez la commande `git stash pop` :

```bash
git stash pop
```

Cette commande restaure les modifications mises de côté et les supprime de la liste des stash.

## Affichage des dépôts distants

Pour afficher les dépôts distants associés à votre dépôt local, utilisez la commande `git remote -v` :

```bash
git remote -v
```

Cette commande affiche les URL des dépôts distants.

## Récupération des modifications

Pour récupérer les modifications d'un dépôt distant sans les fusionner, utilisez la commande `git fetch` :

```bash
git fetch
```

Cette commande télécharge les dernières modifications du dépôt distant mais ne les applique pas à votre branche locale.
