# 📊 Pipeline de Data Mining — Segmentation Stratégique des Clients (RFM)

---

## 👤 Informations sur les étudiants
* **Nom et Prénom :** Taregh Kaber
* **Matricule :** C30827
* **Filière :** DA2I
* **Niveau :** L2 — Semestre 4

---

## 📺 Présentation Vidéo et Explication
> 💡 **Note :** 
Pour regarder l'explication des étapes du projet, veuillez cliquer sur le lien ci-dessous :
👉 **[Regarder la vidéo d'explication](Https://drive.google.com/file/d/104P9P2SYVFYnntl7pq6XSNcnIdujYfnW/view?usp=drivesdk)**

---

## 🛠️ Description du Projet
Ce projet consiste à mettre en place un pipeline complet de **Data Mining** pour analyser le comportement des clients d'un site de commerce électronique (*Online Retail*) en utilisant l'algorithme de clustering **K-Means** basé sur la segmentation **RFM** (Récence, Fréquence, Montant).

### 🚀 Technologies Utilisées
* **Langage :** Python 🐍
* **Environnement :** Jupyter Notebook / VS Code 📓
* **Bibliothèques :** Pandas, NumPy, Scikit-Learn, Matplotlib, Seaborn

---

## 📌 Architecture du Pipeline (Les Phases)

### 📂 Phase 1 : Acquisition et Ingestion (Big Data Ingestion)
* Chargement du fichier initial `OnlineRetail.csv`.
* Conversion et sauvegarde au format de stockage en colonnes **Parquet**.
* Analyse comparative des performances de lecture entre CSV et Parquet.

### 🧼 Phase 2 : Data Cleaning
* Analyse du pourcentage des valeurs manquantes.
* Suppression des lignes sans identifiant client (`CustomerID`).
* Élimination des transactions aberrantes (quantités négatives/annulations et prix nuls).
* Création de la variable financière essentielle : $MontantTotal = Quantity \times UnitPrice$.

### 📈 Phase 3 : Feature Engineering (Transformation RFM)
* Agrégation des données transactionnelles pour créer la structure : **Une ligne = Un client**.
* Calcul des 3 indicateurs clés : **Récence (R)**, **Fréquence (F)**, et **Montant (M)**.
* Application d'une transformation logarithmique ($\log(x+1)$) pour corriger l'asymétrie des distributions.
* Normalisation des données à l'aide de `StandardScaler`.

### 🎯 Phase 4 : Clustering et Optimisation
* Recherche du nombre optimal de clusters ($K$) par la **Méthode du Coude** (*Elbow Method*).
* Validation statistique de la qualité de séparation via le **Silhouette Score**.
* Entraînement final du modèle **K-Means**.

### 📊 Phase 5 : Découverte de Connaissances (Data Storytelling)
* Profilage marketing des segments identifiés (Champions, Clients à Risque, Nouveaux Clients).
* Visualisation des résultats et de la séparation des clusters en **2D** et **3D**.

---
