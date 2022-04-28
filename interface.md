---
layout: default
title: 2. Interface Ouali
has_children: true
nav_order: 3
description: "Présentation de l'interface d'Ouali et des outils à disposition"
permalink: /interface
---

# Interface Ouali

On accède à Ouali en naviguant vers [ouali.renouvaud.ch](https://ouali.renouvaud.ch). 

Utilisez vos identifiants Alma habituels pour vous identifier, en prenant soin de choisir le réseau 
(Network Zone, Sciences et Patrimoines, Écoles et Lecture publique) correspondant à votre identifiant.
Veuillez contacter la [Coordination Renouvaud](mailto:coordrnv@renouvaud.ch) si vous rencontrez des
difficultés à vous connecter à Ouali.

## Fonctionnement général

Le système Ouali gère des alignements de notices d'autorité entre un référentiel source et un référentiel cible. Chaque _alignement_
représente une notice d'autorité du référentiel source aligné vers une notice dans le référentiel cible.

Pour construire ces alignements, le système effectue, pour chaque notice du référentiel source, une recherche de notices dans le 
référentiel cible correspondantes qui sont ensuite comparés de manière détaillée au moyen d’un algorithme. 
En fonction des résultats de ces calculs de correspondance, le système va émettre une décision pour la notice source concernée qui 
consistera soit à établir automatiquement soit une décision d'alignement vers une notice correspondante dans le référentiel cible,
soit une décision de non-alignement (il n'y a pas d'équivalence dans le référentiel cible), soit encore de laisser la notice source
en état d’attente d’arbitrage manuel.

Ces éléments en attente d’arbitrage peuvent ensuite être traités au moyen de l’interface d’arbitrage décrite dans ce manuel et ainsi compléter l’alignement.

Chaque utilisateur se voit automatiquement attribuer un ensemble de notices à arbitrer (initialement 25) qu’il peut alors traiter à son rythme, tout en rejetant les cas qu’il n’est pas en mesure de traiter. Au fur et à mesure de l’avancement, des nouveaux éléments sont automatiquement attribués en fin de liste à de sorte à conserver un ensemble contenant toujours au moins 25 éléments jusqu’à ce que la totalité des cas à arbitrer soit traitée. 

Les éléments restent attribués pour une période de 10 jours au maximum (remis à zéro lors de chaque connexion sur Ouali). Ensuite, ils redeviennent disponibles pour être attribués à d’autres utilisateurs.

## Codes de couleur

Lorsqu'une **décision d'alignement** vers une notice du référentiel cible a été effectuée (soit automatiquement soit après arbitrage
manuel), la notice s'affiche en **vert** dans Ouali.

Lorsqu'une **décision de non-alignement** a été effectuée (automatiquement ou manuellement), la notice s'affiche en **rouge**.

Lorsqu'une notice est **en attente d'arbitrage** (aucune décision n'a encore été prise), elle s'affiche en **gris**.

La notice **actuellement sélectionnée** (sur laquelle on travaille) s'affiche en **bleu**.

## Liste des instances

Une fois identifié dans Ouali, la liste des [instances](chantiers#instances-ouali) s'affiche. Cliquer sur le bouton "Arbitrage" pour
ouvrir l'une des instances et débuter le travail d'arbitrage.

![Liste des instances dans l'interface Ouali](/img/interface-liste-instances.png) 

Noter qu'il peut être nécessaire de faire défiler la liste des instances pour les afficher toutes.

## Interface d'arbitrage

Lorsque vous ouvrez une nouvelle instance, la fenêtre suivante s'affiche.

![Interface d'arbitrage Ouali](/img/interface-alignement.png) 

On remarque les éléments d'interface suivants (décrits plus en détail plus loin):

1. Liste des notices à traiter dans le référentiel source
2. Détail de la notice source en cours de traitement (sélectionnée dans la liste 1)
3. Détail de la notice candidate cible (sélectionnée dans la liste 4)
4. Liste des candidats automatiques proposés par Ouali
5. Onglet Recherche pour lancer une recherche manuelle dans le référentiel cible
6. Formulaire d'alignement
7. Barre de progression de l'instance active (nombres d’éléments avec ou sans correspondance et en attente d’arbitrage)
8. Menu d'aide et menu utilisateur (pour se déconnecter)
9. Retour à la liste des instances

Le processus d’arbitrage manuel consiste à sélectionner une notice source à traiter dans les liste des éléments à traiter (1) pour l’analyser (2) ensuite choisir l’entité cible correspondante (3) au moyen de la liste des candidats automatiques (4) ou au moyen d’une recherche manuelle (5). Une fois qu’une entité cible correspondante a été sélectionnée, ou qu’aucune entité cible correspondante n’a pu être identifiée, il est alors possible de définir le détail des informations de correspondance au moyen du formulaire d'alignement (6).

### 1. Liste des notices à traiter

Cet élément d'interface contrôle quelle notice du référentiel source est sélectionnée pour traitement.

L'onglet "Attribués" s'affiche par défaut:

![Liste des notices attribuées](/img/interface-source-attribues.png) 

Cette liste comporte les notices qui ont été attribuées automatiquement à l'usager actif. Les opérations suivantes sont possibles

1. Obtenir des notices attribuées supplémentaries (ajoutées en fin de liste)
2. Rejeter tous les éléments attribués et de recevoir un nouvel ensemble d’éléments attribués
3. Rejeter un élément spécifique et le renvoyer dans le lot général des notices à traiter. C'est l'option à choisir lorsqu'on n'est pas certain de la décision à prendre. La notice sera réattribuée à un autre usager.
4. Cliquer sur une notice dans la liste pour la sélectionner et l'afficher dans la partie 2 de l'interface.
5. Il est également possible de sélectionner ici une notice déjà traitée et ainsi modifier une décision déjà prise (par exemple pour corriger une erreur).

En cliquant sur l'onglet "Tout" on accède à la liste de toutes les notices présentes dans le référentiel source actif. 

![Liste de toutes les notices du référentiel source](/img/interface-source-tout.png) 

On peut ici 

1. rechercher une notice dans le référentiel source par texte ou avec son numéro de notice
2. ou naviguer la liste des notices avec les options de pagination.

Noter que les résultats d'une recherche s'affichent dans la page 1 de la liste. Lorsqu'on fait une recherche dans cet onglet, s'assurer
que la page 1 est sélectionnée.

### 2. Détail de la notice source    

Détail de l’élément source en cours de traitement.

![Notice source en cours de traitement](/img/interface-tab-source.png) 

Les opérations suivantes sont possibles

1. Bouton permettant de basculter entre la vue MARC et l'affichage visuel de la notice source
2. Liste des notices bibliographiques liées et des correspondances existantes. Un clic droit sur l'une de ces notices affiche un menu contextuel avec les deux options suivantes
3. Voir la notice bibliographique liée au format MARC
4. Signaler que la notice d'autorité courante a été attribuée par erreur à cette notice bibliographique. Il peut arriver que l'on tombe sur un cas de figure où une notice d'autorité a été attribuée par erreur. On peut ainsi signaler une telle erreur pour qu'elle soit corrigée par la suite. Cette opératio a pour effet d'ajouter un sous-champ "vedette incorrecte".
5. Cette icône indique la catégorie de notice dont il s'agit (ici une notice de type lieu/géographique)
6. Numéro de la notice dans le référentiel source. C'est le numéro à noter si l'on relève une question ou un problème avec une notice particulière et qu'on souhaite le transmettre à quelqu'un. Ce numéro unique permet de retrouver la notice en question avec plus de certitude qu'avec la vedette.

### 3. Détail de la notice cible   

Détail de la notice cible actuellement sélectionnée dans la liste 4. Les éléments d'interface sont ici identiques au panneau précédent (notice source), à l'exception du menu contextuel dans la liste des notices bibliographiques liées, qui n'est pas disponible ici.

### 4. Liste des candidats

Liste des candidats proposés par Ouali. La petite icône affichée donne une indication du niveau de confiance attribué par Ouali à chacun des candidats affichés: confiance élevée (vert), confiance partielle (organge), confiance basse (rouge).

Cette liste n'est pas exhaustive, elle ne reprend que les candidats proposés par l'alogrithme d'Ouali. Pour rechercher l'ensemble du
référentiel cible, basculer dans l'onglet de recherche (section suivante).

### 5. Recherche dans le référentiel cible

Onglet permettant d’accéder à la recherche directe, si les candidats automatiques ne semblent pas satisfaisants.

### 6. Panneau de correspondance
Ce panneau donne une vue d’ensemble des diverses sources de correspondance existante pour cet objet. Cela comprend:
La couleur de l’en-tête indique l’état d'alignement pour cet élément: bleu = aucune information de correspondance définie (en arbitrage), vert = alignement avec un élément cible défini, rouge = décision de non-alignement (rejet).

* Alignement utilisateur: correspondance (non-correspondance) précise définie explicitement par un utilisateur (correspondance manuelle)
* Alignement externe: alignement pré-existant tels que VIAF ou provenant d’un projet local
* Recherche automatique: algorithme de recherche automatique de correspondance dans le réservoir cible à partir des libellés de l’objet source. Cet algorithme fournit un ensemble de candidat classé en trois catégories: valide (vert), fort (orange) ou faible (rouge)

La partie inférieure (décision) indique la correspondance effectivement établie par le système. Celle-ci est définie par un algorithme de décision à partir des informations existantes. En l’état, l'algorithme sélectionne la première correspondance valide parmi les 3 sources d’informations prises dans l’ordre, soit:

1. Si une correspondance utilisateur existe, alors celle-ci sera systématiquement sélectionnée
2. Sinon, si une correspondance externe existe, alors celle-ci est sélectionnée
3. Sinon, si la recherche automatique produit un unique candidat valide, alors celui-ci sera sélectionné
4. Sinon, aucune correspondance (ou non correspondance) ne sera établie pour cet élément qui sera alors considéré comme devant être attribué pour un arbitrage utilisateur

Finalement, le panneau comprend également un bouton permettant de définir, ou d’éditer, les informations de correspondance utilisateur.