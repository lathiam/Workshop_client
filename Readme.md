Travaux Pratiques de Machine Learning basé sur un projet de classification de prêts bancaires
Ce travail pratique a pour but de guider les apprenants dans toutes les étapes d'un projet de classification supervisé en machine learning. Il est basé sur un jeu de données contenant des informations sur des demandes de prêts bancaires.

Description des données :
Ce dataset contient des informations sur quatre demandeurs de prêt différents. Chaque entrée comprend des informations telles que l'identifiant du prêt, le sexe, l'état civil, les personnes à charge, le niveau d'études, le statut d'indépendant, les revenus du demandeur, les revenus du codemandeur, le montant du prêt, la durée du prêt, l'historique de crédit et la superficie du bien.


À travers les étapes suivantes, vous serez amené à explorer, prétraiter, modéliser et évaluer les données pour prédire l'octroi d'un prêt.
ÉTAPE 1 : Analyse exploratoire des données (EDA)
Comprendre la structure du dataset Merged_Loan_Dataset.csv et explorer les différents types de variables qu'il contient
Utiliser la commande loan_df.info pour identifier les types de variables et repérer les valeurs manquantes
Distinguer les variables continues comme ApplicantIncome ou LoanAmount et les variables discrètes comme Gender ou Loan_Status
Explorer les statistiques descriptives des variables continues à l'aide de la méthode describe
Visualiser les distributions des variables continues à l'aide de sns.histplot pour mieux comprendre leur comportement et identifier éventuellement des valeurs aberrantes
Réfléchir à la différence entre variable continue et variable discrète, et à l’impact que cela peut avoir sur le choix du modèle et des prétraitements
Analyser les éventuelles anomalies dans les revenus ou les montants demandés
ÉTAPE 2 : Nettoyage des données
Nettoyer les données pour les rendre exploitables par les modèles
Commencer par supprimer la colonne inutile Set avec drop(columns=['Set'])
Rechercher les valeurs manquantes grâce à info ou isnull().sum()
Définir une stratégie claire pour traiter les NA selon leur importance : suppression, imputation par la moyenne, la médiane, ou autre
Vérifier s’il existe des doublons et choisir de les supprimer si nécessaire
ÉTAPE 3 : Feature Engineering
Transformer les variables qualitatives et créer de nouvelles variables utiles pour la prédiction
Encoder les variables qualitatives avec pd.get_dummies ou LabelEncoder
Séparer les features explicatives de la variable cible Loan_Status
Facultatif : ajouter des variables dérivées comme TotalIncome qui combine les revenus principal et co-applicant
Analyser quelles nouvelles variables peuvent apporter une meilleure précision au modèle
Justifier les choix d'encodage effectués
ÉTAPE 4 : Entraînement de modèles (baseline et modèles avancés)
Expérimenter plusieurs modèles de classification pour comparer leurs performances
Diviser les données en ensemble d'entraînement et de test avec train_test_split
Entraîner plusieurs modèles du code fourni : DecisionTreeClassifier, RandomForestClassifier, SVC, KNeighborsClassifier, LogisticRegression
Comparer les performances des modèles à l’aide de f1_score 
Choisi le(s) modèle(s) le(s) plus performant(s) et analyser pourquoi il(s) fonctionne(nt) mieux que d’autre(s)


