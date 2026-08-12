# Atelier NumPy — Analyse et préparation de données de capteurs IoT

Manipulation, analyse et préparation de données numériques avec NumPy, dans une optique Data Science et Machine Learning.

## Présentation

Cet atelier met en pratique NumPy, bibliothèque fondamentale de l'écosystème Python pour la Data Science et le Machine Learning.

Le projet simule l'analyse de données issues de capteurs IoT installés dans plusieurs bâtiments (relevés de température à différentes heures), avec pour objectif de maîtriser les opérations permettant de créer, manipuler, analyser et préparer ces données avant leur utilisation dans un futur modèle de détection d'anomalies.

## Compétences développées

| Domaine | Compétences |
| --- | --- |
| Manipulation | Tableaux 1D/2D, indexation, slicing, reshape, concaténation |
| Analyse | Filtrage booléen, détection d'anomalies, statistiques (min, max, mean, std) |
| Performance | Vectorisation, broadcasting |
| Préparation ML | Standardisation, normalisation Min-Max |

## Concepts clés abordés

### 1. Listes Python vs tableaux NumPy

Comparaison des comportements lors d'opérations numériques. NumPy permet des opérations vectorisées sur l'ensemble des valeurs.

```python
temperatures = np.array([24.5, 25.1, 26.3, 27.0, 25.8])
temperatures * 2
```

### 2. Création de tableaux

Principales méthodes étudiées :

```python
np.array()
np.zeros()
np.ones()
np.full()
np.eye()
np.arange()
np.linspace()
np.random
```

### 3. Exploration des tableaux

```python
array.ndim
array.size
array.dtype
array.shape
```

Ces propriétés donnent le nombre de dimensions, le nombre total d'éléments, le type des données et la forme du tableau.

### 4. Indexation et slicing

```python
array[0]
array[-1]
array[8:13]
array[:, 10]
```

### 5. Filtrage booléen et détection d'anomalies

```python
anomalies = temperatures > 35
```

Création d'un masque booléen pour identifier les valeurs dépassant un seuil défini.

### 6. Manipulation des dimensions

```python
array.reshape()
array.flatten()
array.T
```

### 7. Concaténation

```python
np.concatenate()
np.vstack()
```

Utilisée pour regrouper les mesures provenant de plusieurs bâtiments et capteurs.

### 8. Calcul scientifique et statistiques

```python
np.min()
np.max()
np.sum()
np.mean()
np.median()
np.var()
np.std()
```

L'argument `axis` est essentiel pour les tableaux multidimensionnels :

```python
np.mean(data, axis=0)
np.mean(data, axis=1)
```

`axis=0` donne un résultat par colonne, `axis=1` donne un résultat par ligne.

### 9. Standardisation des données

La standardisation transforme les données pour qu'elles soient centrées autour de 0, avec un écart-type égal à 1.

```text
z = (x - moyenne) / ecart_type
```

```python
mean = np.mean(data)
std = np.std(data)
data_standardized = (data - mean) / std
```

Utile pour mettre sur une échelle comparable des variables dont les valeurs initiales sont très différentes (température, pression, consommation).

### 10. Normalisation Min-Max

La normalisation Min-Max ramène les données dans un intervalle donné, généralement [0, 1].

```text
x' = (x - xmin) / (xmax - xmin)
```

```python
minimum = np.min(data)
maximum = np.max(data)
data_normalized = (data - minimum) / (maximum - minimum)
```

### 11. Standardisation vs normalisation

| Technique | Résultat | Formule |
| --- | --- | --- |
| Standardisation | moyenne proche de 0, écart-type proche de 1 | (x - moyenne) / ecart_type |
| Normalisation Min-Max | valeurs généralement entre 0 et 1 | (x - xmin) / (xmax - xmin) |

Le choix dépend de la nature des données et de l'algorithme de Machine Learning utilisé.

### 12. Conversion des données

```python
temperatures_fahrenheit = temperatures * 9 / 5 + 32
```

Autre illustration de la vectorisation NumPy.

### 13. Broadcasting

```python
correction = np.array([1, -0.5, 0.2])
mesures_corrigees = temperatures_3x3 + correction
```

Applique automatiquement une correction différente à chaque capteur, sans boucle `for`.

### 14. Pipeline de préparation des données

```text
Donnees brutes
Exploration
Nettoyage et filtrage
Detection d'anomalies
Transformation
Standardisation ou normalisation
Donnees preparees
Machine Learning
```

L'objectif n'est pas seulement d'apprendre des fonctions NumPy, mais de comprendre comment préparer des données numériques pour le Machine Learning.

## Technologies utilisées

Python, NumPy, Jupyter Notebook, Git, GitHub.

## Structure du dépôt

```text
Atelier-NumPy-Capteurs-IoT-ML/
├── atelier_numpy_iot.ipynb
└── README.md
```

## Livrable

Le notebook `atelier_numpy_iot.ipynb` contient l'ensemble des manipulations, analyses et transformations réalisées dans le cadre de l'atelier.

## Contexte

Atelier réalisé dans le cadre de la formation Python pour le Machine Learning et l'IA, Orange Digital Center.