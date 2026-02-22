# Analyse de la Performance Vendeurs & Optimisation Retail

## Présentation du Projet

Ce projet propose une solution pour analyser la rentabilité des fournisseurs et l'efficacité de l'inventaire d'une entreprise de retail. L'objectif est de transformer des données transactionnelles brutes en recommandations stratégiques pour maximiser les marges bénéficiaires.

## 🛠️ Stack Technique

* **Langage :** Python 3.x
* **Analyse de données :** Pandas, NumPy
* **Base de données :** SQLite, SQLAlchemy
* **Visualisation :** Matplotlib, Seaborn
* **Statistiques :** SciPy (Tests d'hypothèses T-Test)
* **Environnement :** Jupyter Notebook

## ⚙️ Architecture du Pipeline (ETL)

Le projet est structuré en trois phases clés pour garantir la fiabilité des insights :

1. **Ingestion (`ingestion_db.py`) :** Automatisation du chargement de plusieurs fichiers CSV vers une base de données relationnelle SQLite avec un système de logging rigoureux.
2. **Transformation (`get_vendor_summary.py`) :** Utilisation de requêtes SQL complexes (CTE) pour fusionner les données d'achats, de ventes et de frais de transport.
3. **Analyse & Nettoyage (`Exploratory Data Analysis.ipynb`) :** Traitement des valeurs aberrantes, gestion des types de données et calcul des KPI.

## 📈 Indicateurs Clés de Performance (KPI) calculés

* **Gross Profit :** Revenus nets après déduction des coûts d'achat.
* **Profit Margin (%) :** Rentabilité relative par marque et par vendeur.
* **Stock Turnover :** Ratio de rotation des stocks pour identifier les produits "dormants".
* **Sales-to-Purchase Ratio :** Évaluation de l'efficacité de l'approvisionnement.

## 🔍 Analyses Statistiques & Résultats

* **Analyse de corrélation :** Identification des facteurs influençant la rentabilité nette (impact des remises vs volume).
* **Validation Statistique :** Application d'un **T-Test** pour confirmer de manière significative la différence de performance entre les segments de vendeurs.
* **Impact du "Bulk Purchasing" :** Démonstration par les données que les achats en gros réduisent le coût unitaire de **X%** (insère ton chiffre ici).

## 🚀 Comment utiliser ce projet

1. **Cloner le repo :** `git clone https://github.com/ton-pseudo/nom-du-repo.git`
2. **Installer les dépendances :** `pip install -r requirements.txt`
3. **Lancer l'ingestion :** Exécuter `python ingestion_db.py` pour créer la base `inventory.db`.
4. **Explorer :** Ouvrir les notebooks Jupyter pour visualiser les analyses.

## 💡 Conclusions Business

* Identification des vendeurs à risque (faible rotation de stock).
* Recommandation de révision de la stratégie de prix pour les marques à haute marge mais faible volume.
* Optimisation de la trésorerie via la réduction des stocks invendus identifiés.

---

### Quelques conseils pour booster ton repo :

1. **Captures d'écran :** Ajoute une ou deux images de tes plus beaux graphiques Seaborn dans le dossier du projet et appelle-les dans le README. Un graphique parle plus que 100 lignes de texte.
2. **Fichier `requirements.txt` :** N'oublie pas de créer ce fichier. Tu peux le générer facilement en tapant `pip freeze > requirements.txt` dans ton terminal.
3. **Le fichier `.gitignore` :** Assure-toi d'ajouter `inventory.db` dans ton `.gitignore` si la base de données est trop lourde pour GitHub, ou si tu veux que les utilisateurs génèrent la leur avec ton script.

Est-ce que cette structure te convient ? On peut détailler une partie spécifique si tu le souhaites !
