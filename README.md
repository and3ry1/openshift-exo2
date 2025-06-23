# Exercice Openshift #2 - Déploiement d'une API manipulant des fichiers

Via Opennshift, réaliser le déploiement de l'application [ci-jointe](./app-v1.zip).

Cette application est une API en Node.js fonctionnant via le module Express.js

* L'API écoutera à la variable d'environnement PORT (ou à 3000 par défaut). 
* Pour ses endpoints: 
    * `GET /` qui doit retourner le message **Hello World!**
    * `GET /comments` va lire le contenu du fichier interne de sorte à stocker les ajout éventuels de messages par l'utilisateur
    * `POST /commennts` permet d'envoyer une requête portant un message qui sera ajouté à un fichier interne

La structure du corps de la requête à envoyer à l'API sera la suivante: 

```json
{
    "message": "string"
}
```

Vous devrez donc la déploier dans le cluster Openshift. Pour cela, vous avez le choix entre réaliser un déploiement via l'image ou via le code source (idéalement, faites les deux pour pratiquer). Faites en sorte que l'image fonctionne sur Openshift pour la partie déploiement via une image (attention au rootless!)

Pour lancer l'application localement, il suffit d'avoir node.js d'installé et de faire les lignes de commandes suivantes: 

```bash
npm install # Pour installer les dépendances

npm start # Pour démarrer l'API
```# openshift-exo2
