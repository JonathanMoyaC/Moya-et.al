# Machine Learning models for aiding the decision-making process in emergency departments

##Tabla comparativa de algoritmos

En este script se desarrollará una serie de predicciones basadas en datos del hospital San Juan de Dios Curicó, correspondientes al año 2018 representados por registros de urgencias. El objetivo es predecir, mediante un algoritmo de arboles de desición, la categoría de gravedad de un apciente de urgencias,tomando como input, datos proporcionados por el paciente en la etapa de registro y sus signos vitales registrados en la etapa de triage. Se correrán algoritmos de prodicción tales como árboles y bosques de desición, regresión logística, support vector machines y redes neuronales. Para finalmente evaluar el rendimiento de cada algoritmo en términos de la predicción, mediante indicadores tales como Acuraccy, F1-Score, Curva ROC, Índice de Jaccard y logloss

### Descripción de datos

Los datos utilizados fueros proporcionados por el Hospital San Juan de Dios, Curicó, Chile y corresponden a 4.971 registros de pacientes que asistieron a urgencias durante el periodo comprendido entre el 1 de enero de 2018 y agosto de 2019, los datos fueron limpiados y transformados en un script desarrollado previamente

Datos:[Base de datos 2018](https://drive.google.com/open?id=1Bp7_MnK6cGwgBuwIq1a8S4DS_0wVDiAD).
Tipo de datos: csv
Las variables presentes en los datos se describen a continuación:

-PAC_EDAD: corresponde a la edad del paciente en enteros
-MOTIVO_CONSULTA: corresponde a la razón por la que el paciente acude al servicio de urgencias string
-MEDIO: corresponde al medio de llegada, mediante el que el paciente acude al servicio de urgencias
-SEXO: corresponde al sexo del paciente
-CAT: corresponde a la categoría de gravedad asignada al paciente en el proceso de Triage
-PRESION_SIST: corresponde la presión sistólica del paciente
-PRESION_DIAST: corresponde la presióndiastólica del paciente
-SATO2: Dato numérico que representa la saturometria del paciente (Nivel de oxigeno en la sangre)
-TEMPERATURA: corresponde a la temperatura corporal del paciente en el momento de la categorización
-GLASGOW: corresponde a al nivel registrado por el paciente en la escala Glasgow
-DM: corresponde si el paciente presenta o no Diabetes Mellitus
-EVA: corresponde si se aplica al paciente una evaluación de vias aéreas
-HGT: corresponde a la medida de azucar en la sangre del paciente
-LCFA: corresponde a si el paciente presenta obstrucción crónica de vías aéreas
-FR: corresponde a la frecuencia respiratoria del paciente
-HTA: corresponde a si el paciente posee Hipertención Arterial
-HORA_INSC: corresponde a la hora en la que el paciente fue categorizado
-MIN_INSC: corresponde al minuto en que el paciente fue categorizado
-TIEMPO_ESPERA_CAT: corresponde al tiempo que espera el paciente luego de ser registrado, para ser categorizado

Cargar paquetes necesarios
```markdown
import pandas as pd
from sklearn import preprocessing
from sklearn import metrics
import sklearn as sk  
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
#métricas de evaluación
from sklearn.metrics import f1_score
from sklearn.metrics import jaccard_similarity_score
from sklearn.metrics import log_loss
from sklearn.metrics import f1_score
from sklearn.metrics import classification_report
#Métodos de tuneo de parámetros
from sklearn.model_selection import GridSearchCV
# Métodos para balancer las clases
from pylab import rcParams
 
from imblearn.under_sampling import NearMiss
from imblearn.over_sampling import RandomOverSampler
from imblearn.combine import SMOTETomek
from imblearn.ensemble import BalancedBaggingClassifier
 
from collections import Counter
```
1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/JonathanMoyaC/Moya-et.al/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
