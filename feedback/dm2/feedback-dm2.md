# Feedback DM2

## Révision

- Le feedback et les corrections demandées ont été bien implémentées!

## Architecture

- L'architecture est bien pensée mais on a demandé un diagramme, pas une description purement textuelle.

## Diagramme de classes

- Il n'y a pas de classe Main apparente pour lancer l'application. 
- Les tâches sont bien réparties dans les controllers. Il aurait été cependant idéal d'ajouter une classe DatabaseService
pour s'occuper purement des opérations de lecture/écriture des données. Les controllers interagiraient alors avec cette
classe pour obtenir les informations voulues.

## Diagramme de séquence

- Certaines flèches à trait plein vers la droite ne font pas d'appels de fonction mais des descriptions textuelles vagues
de ce que la classe appelée va faire. Ça doit être des appels de fonction.
- Les séquences ainsi que les blocs alternatifs utilisés sont cohérents et bien utilisés.

## Choix du design

- Il manque un peu de détail dans la justification. En quoi exactement l'approche MVC sépare les responsabilités principales?
En faisant en sorte que les couches Vue et Modèle puissent être implémentés et maintenus de manière indépendante. 
- Quid de l'objectif de forte cohésion et faible couplage?

## Implémentation

- L'affichage est absolument sublime!
- L'ajout de requêtes de travail marche et est enregistré de sorte à ce que lorsqu'on se déconnecte du résident pour se connecter
en tant qu'intervenant et qu'on regarde la liste des requêtes, la nouvelle requête est là. Mais lorsqu'on éteint l'application
et qu'on la rallume, la nouvelle requête disparaît. Cela est dû au fait que dans votre code vous initialisez les 3 requêtes avec
`RequeteTravailManager.initialiserRequetes();` à chaque fois que l'application est ouverte, et il n'y a pas de sauvegarde dans une base de données ou dans un fichier extérieur.
- Tout le reste est très propre et marche parfaitement!
- L'usage de commentaires anglais et français en même temps rend le code un peu moins clair que voulu.

## Tests unitaires

- Tous les tests passent et sont très pertinents! Bravo!

## Rapport et Git

- Le rapport est un chouïa cassé au niveau de la colonne de contenu.
