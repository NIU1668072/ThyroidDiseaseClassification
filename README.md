# Classificació Tiroidisme

Aquest repositori conté el projecte realitzat per a la classificació multiclasse de pacients amb trastorns tiroïdals. El treball s'ha desenvolupat com a part del curs **Aprenentatge Computacional** a la Universitat Autònoma de Barcelona.

## Descripció del projecte

L'objectiu principal és construir un model d'aprenentatge supervisat capaç de predir l'estat de salut tiroïdal dels pacients en tres categories:

- **Sa**
- **Hipotiroidisme**
- **Hipertiroidisme**

A partir de les dades clíniques i analítiques, es treballa amb diferents estratègies per gestionar la manca de dades i s'implementen diverses tècniques de classificació per obtenir resultats òptims.

## Característiques del dataset

- **Origen**: [Kaggle - Thyroid Disease Data](https://www.kaggle.com/datasets/emmanuelfwerr/thyroid-disease-data/data)
- **Observacions**: 9172 mostres
- **Atributs**: 31 variables (20 booleanes, 8 numèriques, 3 categòriques)
- **Variable target**: Classificació multiclasse, agrupada en tres categories segons la patologia tiroïdal.
- **Tractament de dades**: S'han aplicat diverses estratègies per gestionar valors NaN, com omplir amb valors especials (-1) o discretitzar els atributs.

## Models implementats

Es van entrenar i avaluar diversos models d'aprenentatge supervisat, incloent:

- **Logistic Regression**
- **SVC (Support Vector Classifier)**
- **KNN (K-nearest neighbors)**
- **Decision Tree**
- **Random Forest**
- **Gradient Boosting**
- **XGBoost**

## Mètriques d'avaluació

A causa del desequilibri en les classes del dataset, s'ha utilitzat el **F1-score macro** com a mètrica principal d'avaluació. 

## Resultats

Després d'un primer entrenament i una cerca d'hiperparàmetres s'ha arribat al 0.949 de f1 score

## Organització del projecte

El projecte està estructurat de la següent manera:

```
ThyroidDiseaseClassification/
├── data/                    # Dades utilitzades en el projecte
├── execucions/              # Registres i resultats d'execucions
├── ReportTemplate/          # Plantilla i informe en LaTeX
├── thyroid.ipynb            # Fitxer principal del codi
└── requirements.txt         # Llibreries necessàries
```

## Requisits

El projecte utilitza les següents llibreries:

- Python 3.8+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- xgboost
- time
- os

Per instal·lar totes les dependències, executa:

```bash
pip install -r requirements.txt
```

## Instruccions d'execució

1. **Clona el repositori**:

   ```bash
   git clone https://github.com/lluispanal/classificacio-tiroidisme.git
   cd classificacio-tiroidisme
   ```

2. **Llegeix l'infome**

   En el document `ReportTemplate/informe.pdf` conté una explicació del que s'ha fet al llarg del treball.

3. **Executa el notebook principal**:

   Obre el fitxer `thyroid.ipynb` amb Jupyter Notebook o JupyterLab i segueix les cel·les per preprocessar les dades, entrenar els models i avaluar els resultats. Els gràfics (que també es troben a l'informe) s'aniran mostrant al llarg de l'execució.


## Altres

    Les dades es poden obtenir també a https://www.kaggle.com/datasets/emmanuelfwerr/thyroid-disease-data/data