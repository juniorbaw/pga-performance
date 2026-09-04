# Méthodologie

## Objectif

Identifier les profils associés à la victoire sur le PGA Tour et étudier comment le type de parcours et les conditions météorologiques modifient ces profils.

## Comparaison relative au plateau

Le score brut dépend fortement du parcours, du champ de joueurs et de la journée de jeu. Chaque score est comparé à la moyenne du plateau pour le même tournoi, la même date et le même tour.

```text
écart = score_joueur − moyenne_du_plateau
```

Un écart négatif indique une meilleure performance que la moyenne du plateau.

## Standardisation

Toutes les métriques sont standardisées à l’intérieur de chaque saison :

```text
z = (valeur − moyenne de saison) / écart-type de saison
```

Les métriques pour lesquelles une valeur faible est favorable sont inversées avant le calcul des Z-scores.

## Indice d’adaptation

L’indice d’adaptation combine le niveau standardisé du joueur et les poids observés chez les vainqueurs pour le type de parcours sélectionné :

```text
indice = (poids_drive × z_drive + poids_fer × z_fer + poids_putting × z_putt)
         / (poids_drive + poids_fer + poids_putting)
```

La note finale est un rang relatif de 1 à 99 dans le groupe `saison × terrain`.

## Interprétation

Une note de 85 signifie que le joueur se situe approximativement au 85e percentile des profils de sa saison pour le type de parcours sélectionné.

Elle ne représente ni une probabilité de victoire, ni une baisse de performance de 15 %.
