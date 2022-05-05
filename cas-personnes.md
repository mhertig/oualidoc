---
title: Noms de personne
parent: 3. Règles d'alignement
has_children: false
nav_order: 1
permalink: /personnes
---

# Noms de personne: cas particuliers

Cette page regroupe les procédures d'alignement à suivre pour traiter certains cas particuliers
qui peuvent intervenir dans les instances **noms de personne**.
Ces procédures sont en cours de discussion par le groupe de travail Ouali et sont amenées à évoluer.

## Spécificités du référentiel IdRef

Il faut être attentif au fait qu'IdRef contient des entrées de noms de personne de type "sujet", par exemple pour les personnages
historiques ou fictifs.

IdRef comporte également des notices "auteur-titre" (par exemple _Baudelaire, Charles 1821-1867 Le Spleen de Paris_) qui ne sont
pas distinguées des notices de type "nom de personne". Il est important de ne pas aligner des auteurs vers des auteurs-titre.

Les règles de catalogage utilisés pour la création d'entrée dans IdRef diffèrent de celles utilisées dans les référentiels rnv-mat
ou ATC. Notamment, IdRef utilise la forme francisée pour les noms propres (p.ex. _Louis II roi de Bavière 1845-1886_) alors que les ATC
par exemple utilisent la langue d'origine (_Ludwig II, roi de Bavière_).

Pour plus de détails, [consulter la documentation IdRef](http://documentation.abes.fr/aideidref/accueil/fr/index.html).

## Attention aux homonymes

En général, on recommande de prêter une attention particulière aux notes d'application pour s'assurer qu'il s'agit
de la bonne personne: dates de vie, localisation géographique, discipline, etc.

Les notices bibliographiques liées peuvent également fournir des indices précieux sur la discipline d'un auteur particulier, etc.
S'il n'exite aucune notice bibliographique commune aux notices source et cible, une recherche sur le web ou sur Worldcat peut
être utile pour identifier les autres oeuvres d'un auteur particulier.

## Attention aux notices de type "auteur-titre"

Il est important d'aligner vers une notice cible de même type que la notice source. Ainsi, les notices de type "nom de personne"
ne doivent pas être alignées vers les notices de type "auteur-titre" que l'on trouve dans IdRef.

### Exemple

| Source                      | Cible                                                    |
| --------------------------- | -------------------------------------------------------- |
| Baudelaire, Charles         | Baudelaire, Charles 1821-1867 ([idref:026709635](https://www.idref.fr/026709635)) |
|                             | Baudelaire, Charles 1821-1867 Le Spleen de Paris ([idref:028640454](https://www.idref.fr/028640454))|
|                             | Baudelaire, Charles 1821-1867 Correspondances ([idref:034619933](https://www.idref.fr/034619933))|
|                             | ...                                                      |

**Décision:** Aligner vers le premier candidat car il s'agit de l'entrée d'autorité de type "nom de personne" pour Baudelaire. 
Les autres candidats correspondent à des oeuvres.
