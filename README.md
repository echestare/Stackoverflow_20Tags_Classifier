<a href="https://www.linkedin.com/in/ezequiel-nicolás-starecinch" target="_blank"><img alt="LinkedIn" src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>

<h1 align="center">Stackoverflow: 20 Tags Classifier</h1>
<h3 align="center">Naive-Bayes Classifier for Multinomial Models, Linear Support Vector Machine y <u>Logistic Regression</u>.</h3>

<p align="center"><u>LINK AL NOTEBOOK EN KAGGLE:</u> <a href="https://www.kaggle.com/ezequielstarecinch/stackoverflow-tags20-classifier" target="_blank"><img alt="Kaggle" src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white" /></a></p>

<p align="center"><img src="https://github.com/echestare/Stackoverflow_20Tags_Classifier/blob/main/Snapshots/ML_models.jpg" alt="drawing" width="800"/></p>

<!-- TABLE OF CONTENTS -->
## Índice
<details open="open">
  <summary>Tabla de contenidos: </summary>
  <ol>
    <li>
      <a href="#about-the-project">Sobre el proyecto.</a>
      <ul>
        <li><a href="#project-overview">Resumen del proyecto.</a></li>
        <li><a href="#built-with">Desarrollado con.</a></li>
      </ul>
    </li>
    <li>
      <a href="#installation">Instalación.</a></li>
    </li>
    <li>
      <a href="#stages-overview">Partes del proyecto.</a>
    </li>
    <li>
      <a href="#productionization">Productividad.</a>
    </li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## Sobre el proyecto:
<!-- PROJECT OVERVIEW -->
### Resumen del proyecto:

Cada problema de Clasificación de etiquetas es único. No siempre son las mismas herramientas las más efectivas para llevarlo a cabo.
Por eso, la finalidad de este proyecto es encontrar la herramienta más adecuada para este dataset. Los modelos probados son:

 - Naive-Bayes Classifier for Multinomial Models
 - Linear Support Vector Machine.
 - Logistic Regression.






<!-- BUILT WITH -->
### Desarrollado con:
* **Versión de Python**: 3.8.8
* **Framework**: Kaggle Kernel and Colaboratory Google.
* **Packages**: pandas, numpy, matplotlib, BeautifulSoup, re, os, PIL, wordcloud, NLTK, sklearn.



<!-- INSTALLATION -->
## Instalación 
Clonando el repo
   ```sh
   git clone https://github.com/echestare/Stackoverflow_20Tags_Classifier.git
   ```
En google  colab:
>Suponiendo que ya tiene los permisos de Kaggle. Si no, puede seguir estos pasos: [How to Load Kaggle Datasets Directly into Google Colab?](https://www.analyticsvidhya.com/blog/2021/06/how-to-load-kaggle-datasets-directly-into-google-colab/)

- Primero ir a la dirección del notebook que quiere ejecutar. Por ejemplo:
```sh
   https://github.com/echestare/Stackoverflow_20Tags_Classifier/blob/main/stackoverflow-20tags-classifier.ipynb
   ```
   Y se reemplaza, en la dirección, `github.com` por `githubtocolab.com`. Como a continuación:
```sh
   https://githubtocolab.com/echestare/Stackoverflow_20Tags_Classifier/blob/main/stackoverflow-20tags-classifier.ipynb
   ```
   
- Luego ejecutar en la primera celda (para que se agreguen los archivos extras):

   ```sh
   !git clone https://github.com/echestare/Stackoverflow_20Tags_Classifier
   ```



<!-- stages overview -->
## Partes del Proyecto:

#### Datos:
Originalmente este proyecto había sido aplicado en otro dataset que estaba alojado en Google Cloud Storage, que ya no está disponible, por eso fue adaptado para ser aplicado en un dataset similar alojado en Kaggle: [Facebook Recruiting III - Keyword Extraction](https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction)

El formato es *.csv .

De la misma forma, el trabajo está hecho sólo sobre 20 tags, por lo tanto de las 6M de filas, sólo trabajamos sobre 213K filas.

#### EDA:

Se puede apreciar en el gráfico que la distribución de los datos es notablemente heterogénea

<img src="https://github.com/echestare/Stackoverflow_20Tags_Classifier/blob/main/Snapshots/tags.jpg" alt="drawing" width="500"/>
<img src="https://github.com/echestare/Stackoverflow_20Tags_Classifier/blob/main/Snapshots/wordcloud.png" alt="drawing" width="500"/>

#### Procesamiento de texto:

 - Paso de todos los textos a minúsculas.
 - Quitado de código HTML con BeautifulSoup.
 - Reemplazo de algunos símbolos y remoción de otros.
 - Tokenizado y remoción de Stopwords.

#### División entre Datos de Entrenamiento y Datos de Prueba:

La división se realizó con la herramienta `train_test_split` de la librería de scikit-learn. Se dividió: el 79% de los datos para Entrenamiento y el 30% para Prueba.

#### Clasificador Naive Bayes para modelo Multinomial:
Este modelo tuvo la exactitud más baja, pero sirve como punto de partida.

#### Linear Support Vector Machine
Este algoritmo fue, en su momento reconocido como uno de los mejores algoritmos de clasificación y, de hecho, en este modelo se comportó a la altura.

#### Regresión Logística
Teniendo en cuenta la naturaleza categórica de nuestra clasificación, era inevitable intentarlo con este algoritmo, sin mencionar su potencial de combinación y mejora.

Y así mismo, de los tres modelos entrenados, este dio los mejores valores de exactitud.

#### Resultados

<p align="center"><img src="https://github.com/echestare/Stackoverflow_20Tags_Classifier/blob/main/Snapshots/Accuracies.jpg" alt="drawing" width="500"/></p>




<!-- productionization -->
## Productividad:

Los resultados no son nada malos, sin embargo, este proyecto es tremendamente flexible. Se puede modificar los modelos, agregarles o quitarles cosas y probar con otros modelos. Por ejemplo, sería interesante probar con las bondades del Doc2Vec; agregar una lematización o stemming;  incluso se puede probar con k-nearest o random forest; entre muchas alternativas más.



