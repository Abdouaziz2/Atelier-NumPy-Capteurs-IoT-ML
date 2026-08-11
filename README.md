# Atelier NumPy — Analyse de données de capteurs IoT

Cet atelier met en pratique **NumPy**, une bibliothèque fondamentale de l'écosystème Python pour la Data Science et le Machine Learning.

Le projet simule l'exploitation de données provenant de capteurs installés dans différents bâtiments. Les capteurs mesurent notamment la température et permettent de préparer les données avant leur utilisation dans un futur système de **Machine Learning destiné à détecter des situations anormales**.

L'objectif est de maîtriser les principales opérations NumPy utilisées dans la manipulation et l'analyse de données numériques.

##  Objectifs

- Comprendre la différence entre les listes Python et les tableaux NumPy
- Créer et manipuler des tableaux multidimensionnels
- Maîtriser l'indexation et le slicing
- Utiliser le filtrage booléen pour détecter des anomalies
- Manipuler les dimensions des tableaux
- Fusionner des données avec la concaténation
- Effectuer des calculs statistiques
- Standardiser et normaliser des données
- Comprendre et utiliser le broadcasting
- Préparer des données numériques pour des traitements de Machine Learning

##  Contenu de l'atelier

### 1. Listes Python vs NumPy
Comparaison des comportements des listes Python et des tableaux NumPy lors des opérations numériques.

### 2. Création de tableaux
Utilisation de différentes méthodes de création :

- `np.array()`
- `np.zeros()`
- `np.ones()`
- `np.full()`
- `np.eye()`
- `np.arange()`
- `np.linspace()`
- `np.random`

### 3. Exploration des tableaux
Analyse des propriétés d'un tableau :

- dimensions (`ndim`)
- nombre d'éléments (`size`)
- type des données (`dtype`)
- forme (`shape`)

### 4. Indexation et slicing
Extraction de mesures spécifiques à partir des données de température.

### 5. Filtrage booléen
Identification des températures dépassant certains seuils afin de détecter des situations potentiellement anormales.

### 6. Manipulation des dimensions
Travail avec des matrices représentant plusieurs capteurs et différentes mesures temporelles.

### 7. Concaténation
Fusion des données provenant de plusieurs bâtiments et de plusieurs capteurs.

### 8. Calcul scientifique
Calcul de :

- minimum
- maximum
- somme
- moyenne
- médiane
- variance
- écart-type

L'atelier aborde également la **standardisation**, la **normalisation Min-Max** et la conversion Celsius/Fahrenheit.

### 9. Broadcasting
Application automatique de valeurs de calibration aux mesures de plusieurs capteurs.

### 10. Bonus
Ajout de fonctionnalités permettant d'aller plus loin dans l'analyse des données.

##  Technologies utilisées

- Python
- NumPy
- Jupyter Notebook
- Git
- GitHub

##  Structure du dépôt

```text
Atelier-NumPy-Capteurs-IoT-ML/
│
├── atelier_numpy_iot.ipynb
└── README.md
