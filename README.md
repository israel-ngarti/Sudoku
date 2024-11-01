# Projet SUDOKU

## Description du Projet

Le projet **SUDOKU** est un algorithme Python capable de résoudre une grille de sudoku de base. Il utilise des classes et des méthodes pour modéliser et résoudre une grille de sudoku, en appliquant différentes stratégies pour propager des valeurs et réduire les domaines possibles de chaque cellule.

## Table des Matières

- [Description du Projet](#description-du-projet)
- [Auteurs](#auteurs)
- [Fonctionnalités](#fonctionnalités)
- [Installation et Dépendances](#installation-et-dépendances)
- [Utilisation](#utilisation)
- [Fichiers du Dépôt](#fichiers-du-dépôt)
- [Licence](#licence)

## Auteurs

- **Corentin Charpentier**
- **Aya Fergach**
- **Version** : 1.0
- **Date** : 2023-11-17

## Fonctionnalités

Le programme propose les fonctionnalités suivantes :

1. **Classe Cell** : Représente une cellule d'une grille de sudoku, avec des attributs tels que l'identifiant, la valeur, le domaine de valeurs possibles et l'état de verrouillage.
   - `line()`, `column()` et `square()` permettent d'identifier la ligne, colonne, et carré d'une cellule.
   - `remove_value()`, `update_value()`, `update_domain()` et `reduce_domain()` gèrent les mises à jour du domaine.

2. **Classe Sudoku** : Implémente les méthodes nécessaires pour résoudre une grille de sudoku, incluant :
   - `reset()`, `grid_parser()` et `set_values()` pour initialiser et mettre à jour la grille.
   - `line()`, `column()`, et `square()` pour récupérer les voisins d'une cellule.
   - `propagate()`, `find_unique()`, et `find_pairs()` pour appliquer des stratégies de résolution.

3. **Méthode de Résolution** : La méthode `solve()` permet de résoudre la grille de sudoku en utilisant différents niveaux d'algorithmes :
   - Niveau 1 : Résolution en utilisant uniquement les valeurs uniques.
   - Niveau 2 : Utilise les paires de valeurs pour réduire le domaine.

## Installation et Dépendances

### Prérequis

- Python 3.x
- Dépendances spécifiques disponibles dans `tools` (module custom pour le projet) et le fichier `data/evil_00.txt`.

### Installation

1. Clonez le dépôt :

   ```bash
   git clone https://github.com/israel-ngarti/Sudoku.git
   cd Sudoku
