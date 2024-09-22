# Prédiction et Analyse du Churn des Clients

Ce projet explore les **techniques d'analyse de données** et de **machine learning** pour prédire la résiliation des abonnements (*churn*) dans le secteur des télécommunications. En plus de construire un modèle prédictif, une **analyse exploratoire approfondie** a été réalisée pour identifier les principaux facteurs influençant le churn, fournissant ainsi des insights exploitables pour améliorer la rétention des clients.

## 📂 Dataset

Le dataset utilisé provient de Kaggle : [**Telco Customer Churn**](https://www.kaggle.com/datasets/palashfendarkar/wa-fnusec-telcocustomerchurn).

### Description du dataset :

### Description du dataset :
- **Features** : Informations client, services souscrits, type de contrat, etc.
- **Target** : La variable `Churn` indique si le client a résilié son abonnement (Yes/No).

## 📊 Analyse Exploratoire

Avant d'aborder la modélisation, une **analyse exploratoire des données** a été effectuée pour comprendre les tendances et les facteurs influençant le churn. Cette analyse met en lumière plusieurs relations significatives entre les variables, telles que l'influence des **frais mensuels**, de l'**ancienneté** et du **type de contrat** sur le taux de churn.

Des visualisations graphiques ont été utilisées pour illustrer ces tendances, permettant une interprétation visuelle claire des résultats.

## 🚀 Modélisation et Suréchantillonnage

Les modèles ont été entraînés en utilisant la technique de suréchantillonnage **SMOTE** pour équilibrer les classes (`Churn` et `No Churn`), ce qui a permis d'améliorer la performance des prédictions.

### Méthodes testées :
- **Régression Logistique** : Facilement interprétable, utile pour des insights rapides.
- **Random Forest** : Identifie l'importance des features tout en offrant une bonne robustesse.
- **XGBoost** : Améliore la précision grâce à la méthode de boosting.
- **LightGBM** : Le modèle qui a obtenu les meilleures performances globales.

### Performance des Modèles :
1. **Régression Logistique** :
   - **Accuracy** : 85.94%
   - **Precision** : 85.80%
   - **Recall** : 86.21%
   - **F1-Score** : 86.00%

2. **Random Forest** :
   - **Accuracy** : 85.07%
   - **Precision** : 84.67%
   - **Recall** : 85.73%
   - **F1-Score** : 85.19%

3. **XGBoost** :
   - **Accuracy** : 85.36%
   - **Precision** : 85.49%
   - **Recall** : 85.25%
   - **F1-Score** : 85.37%

4. **LightGBM** *(meilleur modèle)* :
   - **Accuracy** : 86.09%
   - **Precision** : 86.04%
   - **Recall** : 86.21%
   - **F1-Score** : 86.13%

Le modèle **LightGBM** s'est avéré être le plus performant, équilibrant précision et capacité à identifier les churners, et surpassant les autres modèles.

## 🔍 Conclusion

Cette analyse va au-delà de la simple prédiction. Elle inclut une **exploration approfondie des variables** influençant le churn dans les télécommunications, permettant aux entreprises de mieux comprendre leurs clients et de cibler des actions spécifiques pour réduire le taux de résiliation. 

Bien que les modèles de machine learning offrent déjà des performances solides, il serait possible d'**optimiser davantage** les résultats en ajustant les hyperparamètres des modèles, notamment LightGBM. Cependant, cette étape n'a pas été réalisée dans cette analyse afin de rester concentré sur la compréhension des facteurs clés influençant le churn.

## 🛠️ Installation

Pour exécuter ce projet sur votre propre machine, suivez ces étapes :

1. **Cloner le dépôt** :
   ```bash
   git clone https://github.com/Celinamoussaoui/CustomerChurnPrediction.git
   cd CustomerChurnPrediction
