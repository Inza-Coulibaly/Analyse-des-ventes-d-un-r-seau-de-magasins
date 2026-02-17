# 📊 Analyse des ventes d’un réseau de magasins

BUT Science des Données – IUT d’Aurillac – Université Clermont Auvergne

👤 Auteur principal : Dosse Inza COULIBALY
👥 Projet réalisé en groupe

🎯 Objectif du projet

Ce projet vise à analyser la performance de 6 magasins d’un réseau de distribution alimentaire à partir de deux bases de données :

📦 Base Ventes : quantités vendues, prix, promotions, dates
💰 Base Finances : chiffre d’affaires et postes de charges

### L’objectif principal est :

Identifier les facteurs influençant les ventes

Comparer la performance des magasins

Proposer des recommandations stratégiques basées sur des modèles statistiques

🗂️ Données utilisées

📅 Période étudiée : 17 avril 2022 – 26 février 2024
🏪 6 magasins étudiés
📊 Données équilibrées entre magasins

Les données comprennent :

Quantité vendue

Prix unitaire

Promotion (oui/non)

Date (jour, mois, saison)

Chiffre d'affaires

Masse salariale

Dépenses de fonctionnement

Budget publicitaire

🧹 1️⃣ Nettoyage et préparation des données
✔ Traitement des valeurs manquantes

2 040 valeurs manquantes sur la variable Quantité vendue

Imputation réalisée via régression multiple avec le package mice

Conversion en valeurs entières (variable de comptage)

Recalcul du chiffre d’affaires journalier

✔ Traitement des valeurs aberrantes

Correction (et non suppression)

Justification : promotions et pics de demande possibles

📈 2️⃣ Analyse descriptive

L’analyse exploratoire a permis de mettre en évidence :

📌 Impact significatif des promotions

📅 Effets saisonniers marqués

📆 Ventes plus élevées le week-end

🏪 Différences structurelles entre magasins

🔎 Résultats clés

Les promotions augmentent la demande

Les prix sont similaires entre magasins

Le Magasin 6 est le plus performant

Le Magasin 3 est le moins rentable

La rentabilité dépend fortement de la structure des charges

📊 3️⃣ Modélisation statistique
🎯 Variable cible : Quantité vendue (variable de comptage)
Modèles testés :

Régression de Poisson

Régression Gamma

👉 Le modèle Poisson a été retenu (cohérent avec la nature discrète des données).

📌 Modèle final retenu : Modèle avec effet du mois (M5)

Pourquoi ?

Meilleur AIC

Capture finement la saisonnalité

Bon compromis biais/variance

🔍 Résultats majeurs du modèle

🎁 Promotion → +37 à +38 % de ventes

📅 Mois → forte saisonnalité

🏖 Été → référence

🍂 Automne → baisse

🌸 Printemps → forte hausse

📆 Week-end → +15 % environ

💰 Analyse financière (Régression Gamma)

Modélisation du chiffre d’affaires :

Effet significatif du magasin

Seule la masse salariale est significativement liée au CA

Les dépenses de fonctionnement et la publicité ne sont pas significatives

🏪 Comparaison des magasins
Magasin	Performance
Magasin 6	🥇 Plus performant
Magasin 2 & 4	Bon volume
Magasin 3	🔻 Plus faible rentabilité
Magasin 1 & 5	Intermédiaires

Les écarts ne s’expliquent pas par les prix, mais par :

Taille

Organisation

Charges

Emplacement
