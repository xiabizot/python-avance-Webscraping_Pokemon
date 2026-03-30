# Web Scraping Pokemon

Projet de web scraping du site [pokemondb.net](https://pokemondb.net/) pour extraire les donnees du Pokedex complet.

Exercice issu de la plateforme [Python pour la Data Science](https://pythonds.linogaliana.fr/content/manipulation/04a_webscraping_TP.html).

## Fonctionnalites

- Scraping ethique (respect du `robots.txt`, crawl delay de 2s, identification via User-Agent)
- Extraction des caracteristiques de chaque Pokemon (type, taille, poids, stats)
- Construction d'un DataFrame Pandas
- Telechargement et affichage des images des Pokemon

## Apercu

Exemple de donnees extraites :

| National No | Nom       | Type          | HP | Attack | Speed |
|-------------|-----------|---------------|----|--------|-------|
| 001         | bulbasaur | Grass Poison  | 45 | 49     | 45    |
| 004         | charmander| Fire          | 39 | 52     | 65    |
| 007         | squirtle  | Water         | 44 | 48     | 43    |

## Installation

```bash
pip install -r RequirementsPokemon.txt
```

## Utilisation

```bash
python Pokemon.py
```

Le script :
1. Recupere la liste complete des Pokemon depuis le Pokedex
2. Extrait les caracteristiques detaillees des 10 premiers Pokemon
3. Telecharge et affiche les images des 5 premiers Pokemon

## Structure du projet

```
Pokemon/
├── Pokemon.py                 # Script principal
├── RequirementsPokemon.txt    # Dependances
├── README.md
└── pokemon_images/            # Images telechargees (genere a l'execution)
```

## Dependances

| Package          | Role                     |
|------------------|--------------------------|
| `requests`       | Requetes HTTP            |
| `beautifulsoup4` | Parsing HTML             |
| `lxml`           | Parser rapide pour BS4   |
| `pandas`         | Manipulation de donnees  |
| `scikit-image`   | Lecture d'images         |
| `matplotlib`     | Affichage d'images       |
