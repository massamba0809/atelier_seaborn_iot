# Atelier Seaborn — Analyse de capteurs IoT

Ce projet fait partie d'une série d'ateliers data. L'idée ici : prendre des données
de capteurs IoT installés dans plusieurs bâtiments (température, humidité, pression,
consommation énergétique...) et les explorer avec Seaborn pour en tirer des
observations concrètes.

## Ce que fait le projet

Le notebook part d'un simple fichier CSV et avance étape par étape :

- chargement et vérification des données
- distribution des températures (histogrammes, courbes de densité, boxplots, violin plots)
- comparaison entre les 4 bâtiments (B001 à B004)
- comptage des états des capteurs (OK / ALERTE / ERREUR)
- relation entre température et consommation énergétique
- corrélations entre toutes les variables numériques
- une analyse multivariée globale avec un pairplot
- un bonus sur l'évolution de la température selon l'heure de la journée

Chaque partie répond aux questions posées dans l'énoncé (valeurs extrêmes, bâtiment
le plus problématique, variables les plus corrélées, etc.) directement dans le notebook.

## Ce qu'on en retient

Le bâtiment **B004** ressort clairement comme le plus à surveiller : c'est celui
qui a les températures les plus dispersées, les valeurs les plus extrêmes, et le
plus grand nombre d'alertes. Le lien entre température et consommation existe
mais reste modéré (pas de relation ultra forte). Les autres variables (humidité,
pression) n'apportent presque rien en termes de corrélation.

## Structure du projet

```
atelier_seaborn_iot/
├── data/
│   └── mesures_capteurs.csv
├── notebooks/
│   └── atelier_seaborn_iot.ipynb
└── exports/
    └── graphiques exportés en PNG et PDF
```

## Pour lancer le notebook

```bash
pip install pandas numpy seaborn matplotlib jupyter
jupyter notebook notebooks/atelier_seaborn_iot.ipynb
```

## Outils utilisés

Python, Pandas, NumPy, Matplotlib, Seaborn.
