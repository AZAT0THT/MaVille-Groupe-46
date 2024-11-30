# Feedback DM1

Disclaimer : Tout ce qui est mentionné dans le feedback sont les points et les détails à améliorer. Si des aspects du devoir n'ont pas été critiqués, c'est qu'ils sont déjà bons.

## Glossaire

- Il manque des définitions importantes comme "Code de la ville" et "Projet/statut d'un projet".
- La définition de "notification" manque la notion de personnalisation, surtout dans le contexte spécifique de notre application.
- Le glossaire est fait pour clarifier les termes techniques spécifiques à l'application et son domaine. On n'y définit pas les cas d'utilisation, cela est fait dans le diagramme et les scénarios.
- Certaines définitions manquent de clarté, comme "Signaler un problème à la ville" qui n'indique pas quels types de problèmes peuvent être reportés. La définition donnée est trop générale.

## Diagramme de CUs

- L'appli système n'est pas un acteur secondaire valide. Le gros rectangle lui-même représente le système, donc il interagit déjà de près ou de loin avec tous les CUs sans avoir à les relier à un acteur secondaire qui le représenterait.
- L'inscription en tant que résident/intervenant n'est pas une extension à la connexion. Ce sont 3 CUs distincts (connexion, inscription résident et inscription intervenant).
- L'inscription en tant qu'intervenant doit appeler la ville comme acteur secondaire car la ville doit vérifier que le code fourni est valide.
- Il manque une relation <<include>> pour les cas d'utilisation dans lesquels une notification est impérativement envoyée, comme lorsqu'un projet est initié dans un quartier dans lequel un résident a activé les notifications.

## Scénarios

- Le CU "Participer à la planification des travaux" en fait trop pour un seul CU mais le scénario satisfait bien l'objectif donné. L'idéal est de séparer les actions les plus importantes en différents CUs. Ce problème de complexité est présent dans plusieurs autres CUs.

## Diagramme d'activités

- Tous les CUs nécessitent d'être connecté avant de pouvoir les exécuter donc dans le flot du diagramme d'activités, il faut forcer l'utilisateur à se connecter avant de pouvoir brancher vers tous les autres CUs (sauf l'inscription). Vous essayez de faire une boucle en passant par l'inscription/connexion avant de revenir à l'ouverture de l'application mais ça ne marche pas parce que dans votre diagramme, le résident a le choix de directement faire "Soumettre une requête de travail" par exemple.

## Analyse

### Risques 

Bien!

### Besoins non-fonctionnels

- Les justifications doivent contenir plus de contexte spécifique à l'application. Mais le reste est correct.

### Besoins matériels

- On doit aussi considérer les besoins matériels de l'utilisateur pour lancer l'application (en l'occurrence, un ordinateur avec Java).

### Solution de stockage

- Il faut parler de l'architecture de stockage? Partagée, distribuée?

### Solution d'intégration

- Quelles APIs? La clarté de l'explication de l'intégration n'est pas assez claire, il manque du contexte concret sur la façon dont ça améliorerait les services. 

## Git

Bien!

## Prototype

- Il manque l'option de se déconnecter dans le menu principal.

## Rapport

Bien!