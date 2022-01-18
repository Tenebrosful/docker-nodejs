# Projet modèle de back end micro services (Docker + Node.js)

IUT Nancy Charlemagne / Développement de services Back End avec Node.js et Docker 

## Consignes 

### Installation des dépendances NPM

- Avant toute utilisation d'une API Node.js, installer les dépendances NPM (cf. "commandes utiles", ci-dessous).

- Ne jamais installer les dépendances NPM localement. Toujours installer les dépendances NPM depuis le contexte du container.

### Variables d'environnement à configurer pour chaque service

- ./service/.env

## Commandes utiles

- Installer les dépendances NPM :
`docker-compose run <nom-du-service> npm install`

- Exécuter des commandes bash directement au sein du container :
`docker exec -ti <nom-du-service> bash`

ou

`docker-compose run <nom-du-service> bash`

- Démarrer les services :
`docker-compose up`

- Démarrer les services et reprendre la main dans le terminal :
`docker-compose up -d`

- Ré-initialiser les containers :
`docker-compose down`

- Consulter l'API (le service doit être lancé)
`curl -i localhost:3333`

- Pour supprimer un dossier verrouillé (ex : un volume créé par Docker et appartenant à l'utilisateur root), attribuer la propriété du dossier concerné à l'utilisateur courant :
`sudo chown -R $USER:$USER <nom-du-dossier>`

`sudo rm -rf <nom-du-dossier>`

### Nodemon

Si le hot reloading ne fonctionne pas, adapter la commande "watch" du fichier ./service/api/package.json :

`nodemon -L ./bin/www`

## Adminer

- serveur = MYSQL_HOST (cf. ./service//env/)
- mot de passe = MYSQL_PASSWORD (.cf ./service/.env/)

---

__Alexandre Leroux__

- alex@sherpa.one
- https://sherpa.one
- sherpa#3890
- https://github.com/sherpa1/

_Enseignant vacataire à l'Université de Lorraine_

- IUT Nancy-Charlemagne (LP Ciasie)

- Institut des Sciences du Digital, Management & Cognition (Masters Sciences Cognitives)