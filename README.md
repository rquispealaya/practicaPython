# practicaPython

import pandas as pd

import numpy as numpy

import matplotlib.pyplot as plt

import seaborn as sb

import statsmodels.api as sm


# leer archivo de Git

url='https://raw.githubusercontent.com/lorey/list-of-countries/master/csv/countries.csv'

df=pd.read_csv(url,sep=";")

# mostrar las 5 primeras filas del df

print(df.head(5))

# Cantidad de Registros en el DataSet

total_filas=len(df.axes[0])

print("Numero de Registros: " + str(total_filas))

# Mostrar columnas vacias o nulos del Dataset

df.isnull().sum()

# Mostrar columnasmas importantes de dataset

df.describe()

# Analizar si existe correlación en los datos

corr = df.set_index('alpha_2').corr()

sm.graphics.plot_corr(corr,xnames=list(corr.columns))

plt.show()

# Columnas de Salida

print(df.head(5))

df_pop_an = df[df["currency_code"] == 'EUR']

print(df_pop_an.head())

df_pop_an.drop(['currency_code'],axis=1)['population'].plot(kind='bar')

















******************************************************************


aws cloudsearch create-domain --domain-name [YOUR_DOMAIN_NAME]
