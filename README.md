***/ TP Git – Gestion d’un projet “Sandwich” /***

## Objectif:
Ce projet illustre les principales commandes Git à travers un exemple simple : la construction progressive d’un fichier burger.txt, représentant les ingrédients d’un sandwich.
Chaque étape correspond à une action Git (init, add, commit, log, reset, checkout, push, clone…).

## 1-Configuration globale de Git:

Avant de commencer, il est nécessaire de configurer l’identité de l’utilisateur (nom et email).
Ces informations seront associées à chaque commit afin d’identifier l’auteur des modifications.

![WhatsApp Image 2026-02-22 at 21 09 51](https://github.com/user-attachments/assets/e933fb37-5b07-46e8-9846-9f7b46524acc)

## 2-Création du projet et initialisation du dépôt Git

Cette capture montre les toutes premières étapes de création du projet :

Création du dossier sandwich avec la commande mkdir.
Accès au dossier avec cd sandwich.
Initialisation d’un nouveau dépôt Git avec git init.
Vérification de l’état du dépôt avec git status (aucun commit existant).
Création du fichier burger.txt.
Ajout du premier contenu dans le fichier : Pain du bas.

![WhatsApp Image 2026-02-22 at 21 10 37](https://github.com/user-attachments/assets/ebf805c0-7859-48da-82a0-b350bfdb0f17)


## 3-Initialisation du dépôt et premier commit

Cette capture montre les premières étapes du projet avec Git :

Vérification de l’état du dépôt avec git status (aucun commit existant).
Détection du fichier non suivi burger.txt.
Ajout du fichier à la zone de staging avec git add burger.txt.
Vérification des fichiers prêts à être commités.
Création du premier commit avec le message
Initialisation du sandwich : ajout du pain du bas.

![WhatsApp Image 2026-02-22 at 21 12 02](https://github.com/user-attachments/assets/fc271424-3362-4d52-bbe4-9aa9a8de73c3)


## 4-Visualisation des modifications avec git diff:

Cette capture montre qu’après avoir ajouté la ligne **"Salade fraîche"** dans `burger.txt` :

- `git diff` affiche les modifications non ajoutées.
- Après `git add`, `git diff` n’affiche plus rien.
- `git diff --cached` montre les changements prêts à être commit.

![WhatsApp Image 2026-02-22 at 21 22 32](https://github.com/user-attachments/assets/fe604d28-ec09-42c7-85cb-cfc33615fb8a)

## 5-Ajout d’un ingrédient et création d’un commit:
Cette capture montre les étapes suivantes :

- Ajout d’une nouvelle ligne **"Nom de l’ingrédient"** dans `burger.txt`.
- Ajout du fichier à la zone de staging avec `git add`.
- Création d’un commit avec le message **"Ajout de [ingrédient]"**.
- Consultation de l’historique avec `git log`.


![WhatsApp Image 2026-02-22 at 21 26 48](https://github.com/user-attachments/assets/5cf8d0c9-4760-495d-8e41-c096f0e4ae7b)

## 6-Ajout progressif des ingrédients avec plusieurs commits:

Cette capture montre la création de plusieurs commits successifs :

- Initialisation du fichier avec **pain du bas**.
- Ajout de nouveaux ingrédients : **tomate**, **fromage**, puis **steak**.
- Chaque modification est ajoutée avec `git add` puis enregistrée avec `git commit`.
- La commande `git log --graph --oneline --all` permet de voir l’historique des commits.

![WhatsApp Image 2026-02-22 at 21 32 57](https://github.com/user-attachments/assets/4594d822-e165-4ac0-a42d-2cd3e01134df)

## 7-Annulation d’une modification avec git reset et git checkout:

Cette capture montre comment annuler une modification :

- Ajout de nouveaux ingrédients (**steak** puis **sauce**) avec des commits.
- Ajout de **ananas** puis vérification avec `git status`.
- Utilisation de `git reset HEAD burger.txt` pour retirer le fichier de la zone de staging.
- Utilisation de `git checkout -- burger.txt` pour annuler la modification locale.
- Consultation de l’historique avec `git log --oneline`.

![WhatsApp Image 2026-02-22 at 21 37 51](https://github.com/user-attachments/assets/0600d5ff-1c6c-4af9-b096-1b74f0683d54)

## 8-Passage en mode HEAD détaché:

Cette capture montre le passage à un ancien commit avec `git checkout 3a06207`.

- Git indique que l’on est en **detached HEAD**.
- Cela signifie que l’on consulte une version passée du projet.
- Les modifications faites ici ne sont pas liées à une branche tant qu’on n’en crée pas une.

  ![WhatsApp Image 2026-02-22 at 21 38 19](https://github.com/user-attachments/assets/bf46775d-6162-49df-b42e-808ca922d59c)

## 9-Envoi du projet sur GitHub et clonage

Cette capture montre les étapes de travail avec un dépôt distant :

- Création d’un commit pour ajouter le fichier `description.txt`.
- Envoi du projet vers GitHub avec `git push origin main`.
- Création d’un nouveau dossier puis clonage du dépôt avec `git clone`.

![WhatsApp Image 2026-02-22 at 21 39 15](https://github.com/user-attachments/assets/686b5d98-f51d-4582-b3f6-12a884993946)


## 10-Ajout d’un fichier et mise à jour du dépôt distant:

Cette capture montre les étapes de modification et d’envoi d’un fichier vers GitHub :

Ajout d’un nouveau contenu dans le fichier burger.txt avec la commande echo.
Ajout du fichier à la zone de staging avec git add burger.txt.
Création d’un commit avec le message feat: ajout sauce depuis le clone.
Envoi des modifications vers le dépôt distant avec git push origin main.

![WhatsApp Image 2026-02-22 at 21 39 51](https://github.com/user-attachments/assets/c0b51547-dd04-4f8e-9805-acb2b0f7a2e8)


## 11-Travail avec les branches et fusion (merge)

Ces captures montrent la gestion des branches dans le projet :

Récupération des dernières modifications du dépôt distant avec git pull origin main.
Création d’une nouvelle branche fr-main avec git checkout -b fr-main.
Ajout d’un nouvel ingrédient (Oignons) dans le fichier burger.txt.
Création d’un commit sur la branche fr-main.
Retour sur la branche principale main.
Fusion de la branche fr-main avec git merge fr-main.
Affichage de l’historique des commits avec git log --oneline --graph --all.

![WhatsApp Image 2026-02-22 at 21 40 27](https://github.com/user-attachments/assets/a329a211-29c7-427f-9506-85b0c87fbce5)        


![WhatsApp Image 2026-02-22 at 21 41 45](https://github.com/user-attachments/assets/9b64912b-2457-4b87-81ef-64e5708a174b)



## Conclusion du TP :
Ce projet a permis de valider la maîtrise du cycle de vie complet d'un fichier sous Git, de la gestion locale des versions à la collaboration sur
un dépôt distant (GitHub), tout en pratiquant les bonnes méthodes de travail comme l'atomicité des commits et l'isolation par branches.







