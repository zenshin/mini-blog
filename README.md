# My First Blog!

### utilisation

Dans un terminal:
```
$> cd bdd
$> json-server --watch db.json --port=3030
```

Dans un autre terminal:
```
$> cd public
$> live-server --port=3001
```

Nous avons deux programmes, sur deux ports différents:
- Le port 3030 pour l'API (recherche google)
- Le port 3001 pour le serveur web qui deservira vos fichiers)

### infos serveur HTTP:

Pas grand choses à faire ici, nous verrons cette partie plus tard ;)

### infos schémas des tables de la base de donnée:

articles:
```
{
    "id": 1,
    "author": "Jonathan Collinet",
    "title": "Titre",
    "subTitle": "Sous-titre",
    "date": "05/10/12",
    "content": "Contenu Contenu Contenu Contenu Contenu!"
}
```

comments:
```
{
    "id": 1,
    "articleId": 1,
    "author": "John",
    "date": "06/10/12",
    "content": "Ceci est un commentaire!"
}
```

### infos routes API:

Aujourd'hui, même si vous ne savez pas créer d'API, savoir la consommer fait partie du métier de développeur front-end.

Voici toute les routes disponible sur l'API:

Pour les articles:
```
GET    /articles            // récupère tous les articles
GET    /articles/1          // récupère l'article id(1)
POST   /articles            // envoi un article à enregistrer
PATCH  /articles/1          // modifie l'article id(1)
DELETE /articles/1          // supprime l'article id(1)
```

Pour les commentaires en général:
```
GET    /comments            // récupère tous les commentaires
GET    /comments/1          // récupère le commentaire id(1)
POST   /comments            // envoi un commentaire à enregistrer
PATCH  /comments/1          // modifie le commentaire id(1)
DELETE /comments/1          // supprime le commentaire id(1)
```

Pour les commentaires lié à un article:
```
GET    /articles/1/comments     // récupère tous les commentaires de l'article id(1)
GET    /articles/1/comments/1   // récupère le commentaire id(1) de l'article id(1)
POST   /articles/1/comments     // envoi un commentaire à enregistrer pour l'article id(1)
PATCH  /articles/1/comments/1   // modifie le commentaire id(1) pour l'article id(1)
DELETE /articles/1/comments/1   // supprime le commentaire id(1) de l'article id(1)
```

D'autres routes sont disponible pour faire des liaison

### contenu:

!!!NE PAS SE CONCENTRER SUR LE CSS!!!

Aujourd'hui je sais qu'en CSS vous savez faire des choses, animées ou non.

L'objectif maintenant est de savoir récupérer des données depuis un serveur, et les injecter dans votre DOM.

C'est seulement lorsque votre programme est TOTALEMENT fonctionnel que vous pouvez attaquer le style/design.

Maintenant vous allez faire toute les manipulations nécessaire pour arriver à un mini-blog SANS AUTHENTIFICATION, avec un back-office vous permettant d'administrer tout ça.

En fait ce que vous allez faire, c'est créer/utiliser un CRUD (google).

1) page d'accueil (page de lecture)
    - Un menu avec: "Accueil", "Ajouter un article", "Administrer les articles"
    - Afficher tous les articles.
    - Afficher pour chaque articles, la liste des commentaires.
    - a la fin de la liste de commentaire, un formulaire permettant d'ajouter un commentaire.

2) page "ajouter un article":
    - un formulaire permettant d'ajouter un article au complet avec les champs renseigné dans le schéma (tous).
    - un boutton d'envoi de l'article, qui va envoyer par le biai d'une requete l'article au serveur.
    - une fois l'article envoyé, faire une redirection (front/navigateur) vers la page d'accueil.

3) page "administrer les articles" (page d'edition):
    - Lister tous les articles, sans le contenu (c'est a dire juste le titre, l'autheur, la date et le sous-titre)
    - pour chaque articles (par ligne):
        - une icone "edit" qui lorsqu'on clique dessus, "collapse" l'article pour afficher un formulaire d'edition de l'article
        - une icone "delete" qui lorsqu'on clique dessus, demande par une "confirm" si l'utilisateur est sûr de vouloir supprimer l'article.

### consignes:

Vous devez créer ce blog, le serveur et l'API vous ai fourni, vous avez à coder la partie cliente.

Pour ce faire vous allez manipuler les formulaires, faire des manipulation de DOM, des requetes XHR, ...

N'oubliez pas qu'aujourd'hui vous avez toutes les clefs pour réaliser cet exercice.