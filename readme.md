# DOCKER + NODE.JS + MYSQL

## Variables d'environnement

- ./service/.env

## Commandes utiles

- Installer les dépendances :
`docker-compose run <nom-du-service> npm i`

- Entrer dans le container :
`docker exec -ti <nom-du-service> bash`

- Consulter l'API (le service doit être lancé)
`curl -i localhost:3333`

- Pour supprimer un dossier verrouillé (appartenant à l'utilisateur root), modifier les droits :
`sudo chown -R $USER:$USER <nom-du-dossier>`

`sudo rm -rf <nom-du-dossier>`

## Adminer

serveur = MYSQL_HOST (cf. ./service//env/)
mot de passe = MYSQL_PASSWORD (.cf ./service/.env/)


---

__Alexandre Leroux__

alex@sherpa.one
sherpa#3890

_Enseignant vacataire à l'Université de Lorraine_

- IUT Nancy-Charlemagne (LP Ciasie)

- Institut des Sciences du Digital, Management & Cognition (Masters Sciences Cognitives)