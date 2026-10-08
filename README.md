# Projet NoSQL - CampusCollect

## Equipe

- Etudiant 1 : Oussama Tarfaoui
- Etudiant 2 : a completer
- Etudiant 3 : optionnel
- Etudiant 4 : optionnel

## Idee generale

CampusCollect est une application de click & collect pour un campus universitaire.
Elle permet aux etudiants de commander des repas ou produits disponibles dans
plusieurs points de vente du campus, puis de les recuperer a un creneau donne.

L'application est composee de trois services autonomes qui echangent par
evenements :

- `catalogue-service` : gere les produits, les prix et les stocks disponibles.
- `commande-service` : gere les paniers, les commandes et leur statut.
- `notification-service` : prepare les messages envoyes aux utilisateurs.

## Objectif NoSQL

Chaque service possede ses propres donnees sous forme d'agregats JSON. Pour
eviter un couplage direct entre services, les changements importants sont
diffuses sous forme d'evenements. Les services recepteurs peuvent alors creer ou
mettre a jour des repliques locales des donnees necessaires a leur autonomie.

## Documents du projet

- `docs/services-commandes.json` : services et commandes associees.
- `docs/agregats-services.json` : agregats principaux de chaque service.
- `docs/evenements-replication.json` : evenements entre services et repliques.
- `docs/projection-nouveau-service.json` : projection vers un nouveau service.

## Avancement par etape

### Etape 1 : initier le projet

- Depot Git cree.
- Collaborateur `charroux` invite.
- Description du projet redigee dans ce README.
- Equipe indiquee dans la section `Equipe`.

### Etape 2 : definir les services

Les services et les commandes associees sont definis dans
`docs/services-commandes.json`.

### Etape 3 : definir les agregats

Les agregats principaux de chaque service sont definis dans
`docs/agregats-services.json`.

### Etape 4 : decoupler les services

Les evenements entre services et les repliques locales sont definis dans
`docs/evenements-replication.json`.

Le fichier contient au moins :

- un evenement de creation de replique : `ProduitCree`.
- un evenement de mise a jour de replique : `StockProduitModifie`.

### Etape 6 : projection vers un nouveau service

La projection vers le nouveau `statistique-service` est definie dans
`docs/projection-nouveau-service.json`.

## Depot Git

Le depot distant est disponible sur GitHub :

https://github.com/oussamatarfaoui14-dev/campuscollect-nosql
