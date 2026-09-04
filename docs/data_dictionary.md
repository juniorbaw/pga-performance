# Dictionnaire de données

## Tables de staging

| Table | Grain | Description |
|---|---|---|
| `stg_resultats` | joueur × tournoi | Résultats finaux de tournois nettoyés |
| `stg_tours` | joueur × tournoi × tour | Scores par tour au format long |
| `stg_driving` | joueur × saison | Distance et précision au drive |
| `stg_fer` | joueur × saison | Indicateurs de jeu de fers |
| `stg_putting` | joueur × saison | Indicateurs de putting |
| `stg_meteo` | tournoi × date | Conditions météo journalières |

## Dimensions

| Table | Grain | Description |
|---|---|---|
| `dim_joueurs` | joueur | Table de correspondance entre les noms et `PLAYER_ID` |
| `dim_tournois` | tournoi × saison | Identifiant et informations de tournoi |

## Tables analytiques

| Table | Grain | Description |
|---|---|---|
| `mart_z_driving` | joueur × saison | Z-scores distance et précision, plus composite driving |
| `mart_z_fer` | joueur × saison | Z-scores liés au jeu de fers |
| `mart_z_putting` | joueur × saison | Z-scores liés au putting |
| `int_champ_tournoi` | joueur × tournoi | Niveau du plateau et participations |
| `mart_vainqueurs` | tournoi | Profil relatif du vainqueur face au plateau |
| `mart_evolution` | saison | Évolution de la distance moyenne et des parcours |
| `mart_adequation` | joueur × terrain | Indice d’adaptation au type de parcours |
| `mart_meteo_bandes` | joueur × tournoi × bande météo | Analyse des performances selon le vent |
| `mart_carte_joueur_v3` | joueur × saison × terrain | Source de la fiche joueur Looker Studio |

## Champs de la fiche joueur

| Champ | Description |
|---|---|
| `indice_adaptation` | Rang relatif du joueur au sein de sa saison et du terrain choisi |
| `poids_drive` | Poids attribué au driving pour le terrain sélectionné |
| `poids_fer` | Poids attribué au jeu de fers |
| `poids_putting` | Poids attribué au putting |
| `z_drive` | Niveau standardisé du joueur au driving |
| `z_fer` | Niveau standardisé du joueur au jeu de fers |
| `z_putt` | Niveau standardisé du joueur au putting |
| `badge_principal` | Compétence la plus contributive à l’indice d’adaptation |
| `badges_competence` | Ensemble des badges du joueur |
| `terrain` | `Links`, `Stadium` ou `Parkland` |
