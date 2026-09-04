# Contrôles qualité

Chaque source a été contrôlée avant la modélisation sur quatre dimensions :

- nombre de lignes ;
- unicité de la clé ;
- type de données ;
- distribution et médiane par saison.

## Contrôles appliqués

| Contrôle | Exemple |
|---|---|
| Unicité | Une ligne par `PLAYER_ID × SAISON` dans les métriques joueur |
| Unités | Détection de la vitesse de tête de club multipliée par 100 en 2015 |
| Pourcentages | Harmonisation des fractions, pourcentages numériques et pourcentages texte |
| Grain | Vérification de la relation `tournoi × date × tour` pour la météo |
| Jointures | Taux d’appariement entre les libellés de tournois |
| Orientation | Vérification que les meilleurs joueurs possèdent des Z-scores positifs |
| Reproductibilité | Contrôle des tables créées dans l’historique des jobs BigQuery |
