# Projet NoSQL - CampusCollect

## Equipe

- Etudiant 1 : a completer
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

## Depot Git

Le depot Git local est initialise dans ce dossier. Une fois le depot distant
cree sur GitHub ou GitLab, il faudra inviter l'utilisateur `charroux` comme
collaborateur.
