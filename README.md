# Riesgo_crediticio

# SPANISH
Modelo de Machine Learning para determinar el Credit Score
Se divide en dos partes, una que es el datacleaning del dataset y otra en la que se entrena al modelo.
El dataset está sacado de Kaggle. Un dataset que contiene varias features para poder determinar el riesgo crediticio de un cliente.
El dataset tiene como labels (Y's): Malo, Regular, Bueno. Se divide en 3 clases.

Se inicia con un datacleaning del "raw" dataset, para posteriormente intentar con varios clasificadores y un regresor log de Scikit poder predecir el modelo.
Los mejores resultados se obtuvieron con los modelos de Random Forest Classifier y GradientBoost Classifier.

Pasos del datacleaning:

Se importa el dataset.
Se realiza una exploración de data, observar que columnas tienen valores Nan y sus dtypes, donde se puede ver que hay valores numéricos con dtype object.
Se transforma esos valores numéricos que están como objetos a floats.
Se hace stripping the caracteres inútiles que no dejen transformar valores.
En algunas columnas(x's) como "Payment_of_Min_Amount" se pueden convertir los valores Nan en 0's. Ya que los Nan's se pueden tomar como si fueran NO PAGOS. Esto para no eliminar muchas filas y reducir el tamaño del dataset.
A los valores de la columna Y les doy valores de -1 0 1 a Bad, Mid, Good.
Se realiza en clipping de varias columnas que tienen valores exagerados.
Elimino valores irreales de las columnas categóricas.
Realizo el OneHotEncoding de las columnas categóricas.
Normalizo la data (no la data categórica) 
Guardo el dataset limpio en un archivo .csv

Pasos del modelo:

Realizo las crosss features relevantes y modelo individualmente con todas las cross features para ver cuales tienen mejores niveles de predicción.
Las cross features con bajo nivel predictivo no se toman en cuenta.
Se añade las cross features al dataset y se entrena el dataset con diferentes modelos e hiperparámetros.
Los modelos usados de scikit learn son Gradient Boost Classifier, LogReg, Random Forest Classifier y Hist Boost Classifier.


# ENGLISH
Machine Learning model to predict Credit Score
The code is divided in two parts, one is the datacleaning of the dataset and another to train the model.
The dataset is from Kaggle repository. This dataset contains many features to decide the credit score of a client.
The dataset's labels are Bad, Mid, Good. 3 classes.



The project starts with the datacleaning of the raw dataset, then we train the model with many Scikit classifiers and Log reg to predict the outcome.
The project throws that the best results are from Random Forest Classifier and GradientBoost Classifier.

Datacleaning steps:

import the dataset.
Start with exploring the data to see which columns have Nan values and their dtypes, I found that it exists numeric values with dtype objects.
Transform the numeric values with dtype obect to float.
Strip the columns from useless characters
In some columns (x's) like "Payment_of_Min_Amount" it is possible to convert Nan values into 0's.Those Nan values can be deemed as NOT PAID. I did that in order to not get rid of many dataset rows so I wouldn't reduce the size of the whole dataset.
To the values of the Y column I replace the values to -1 0 1 (bad, mid, good)
Clip the skewed columns
Eliminate unreal values from categorical columns
Apply one hot encoding to categorical columns
Normalize the data (not the categorical)
Save the dataset


Modeling steps:

Do some cross features and train models with each one of the cross features to see which features have better performance
Cross Features with low predictive power are dumped.
Add cross features to the dataset and train the dataset with different models and hyperparametres.
The used models from scikit learn library are  Gradient Boost Classifier, LogReg, Random Forest Classifier y Hist Boost Classifier.




### LINK TO THE DATSET: https://www.kaggle.com/datasets/parisrohan/credit-score-classification
