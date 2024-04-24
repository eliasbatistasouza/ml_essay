<!--- LANGUAGE --->
<h6 align="center"><a href="/README.md">PORTUGUÊS</a> • <a href="/README_en.md">ENGLISH</a>
</h6>

<!--- BANNER --->
<div align="center">
<img src="./docs/report-analysis-flatline.svg" alt="Relatório" height="250px"/>
</div>

## Machine Learning Essay
Estudo de *Machine Learning* com algoritmos de Classificação, Regularização e Clusterização, com o objetivo de entender como diferentes hiperparâmetros, e a separação entre dados de treino, validação e teste, impactam a performance e podem leva ao *overfitting* ou *underfitting* em modelos de *machine learning*.

Para esse estudo foram utilizados conjunto de dados préviamente preparados e separados, prontos para aplicação nos algoritmos.

## Algoritmos
Os algoritmos e os parâmetros utilizados no estudo foram:

### Classificação
- **Algoritmos:** K-Nearest Neighbors, Decision Tree, Logistic Regression e Random Forest;
- **Métricas de Performance:** Accuracy, Precision, Recall, F1 Score.

### Regressão 
- **Algoritmos:** Decision Tree Regressor, Random Forest Regressor, Linear Regression, Linear Regression Lasso, Linear Regression Ridge, Linear Regression Elastic Net, Polynomial Regression, Polynomial Regression Lasso, Polynomial Regression Ridge e Polynomial Regression Elastic Net;
- **Métricas de Performance:** R-Quadrado, MSE, RMSE, MAE, MAPE.

### Clusterização
- **Algoritmos:** K-Means, Affinity Propagation;
- **Métricas de Performance:** Silhouette Score.

## Desenvolvimento
Os valores resultantes desse ensaio foram obtidos a partir da aplicação dos seguintes passos:

1. Treinar o modelo com dados de treino utilizando os parâmetros padrão;
2. Medir a performance do modelo nos dados de treino;
3. Medir a performance do modelo nos dados de validação;
4. Modificar valores dos parâmetros escolhidos para esse ensaio e treinar novo modelo com dados de treino; 
5. Medir performance nos dados de validação;
6. Repetir passos 4 e 5 até encontrar o melhor valor dos parâmetros escolhidos;
7. Unir os dados de treino e validação;
8. Treinar o modelo final com os dados unidos e os melhores valores dos parâmetros;
9. Medir performance do modelo final nos dados de teste.

> :bulb: **Clusterização**  
> Para modelos de clusterização foram utilizadas técnicas como *Elbow Method* para escolher os melhores parâmetros.

## Resultados
Os resultados de performance obtidos para cada modelo foram:

### Algoritmos de Classificação
___
É possível perceber que para a maioria dos modelos de classificação, a performance dos dados de validação ficaram bem próximas a performance dos dados de teste.

<div align="center">
  <h4><b>Dados de Treino</b></h4>
</div>

<div align="center">

| **Model**               | **Accuracy** | **Precision** | **Recall** | **F1 Score** |
|-------------------------|:------------:|:-------------:|:----------:|:------------:|
| **KNN**                 | 0.782        | 0.756         | 0.733      | 0.744        |
| **Decision Tree**       | 1.0          | 1.0           | 1.0        | 1.0          |
| **Random Forest**       | 1.0          | 1.0           | 1.0        | 1.0          |
| **Logistic Regression** | 0.567        | 0.0           | 0.0        | 0.0          |

</div>

<div align="center">
  <h4><b>Dados de Validação</b></h4>
</div>

<div align="center">

| **Model**               | **Accuracy** | **Precision** | **Recall** | **F1 Score** |
|-------------------------|:------------:|:-------------:|:----------:|:------------:|
| **KNN**                 | 0.676        | 0.632         | 0.603      | 0.617        |
| **Decision Tree**       | 0.945        | 0.935         | 0.938      | 0.936        |
| **Random Forest**       | 0.965        | 0.974         | 0.945      | 0.959        |
| **Logistic Regression** | 0.567        | 0.0           | 0.0        | 0.0          |

</div>

<div align="center">
  <h4><b>Dados de Teste</b></h4>
</div>

<div align="center">

| Model                   | Accuracy | Precision | Recall | F1 Score |
|-------------------------|:--------:|:---------:|:------:|:--------:|
| **KNN**                 | 0.688    | 0.648     | 0.635  | 0.642    |
| **Decision Tree**       | 0.948    | 0.940     | 0.941  | 0.940    |
| **Random Forest**       | 0.965    | 0.974     | 0.946  | 0.960    |
| **Logistic Regression** | 0.871    | 0.867     | 0.834  | 0.851    |

</div>

### Algoritmos de Regressão
___
Vemos que nenhum modelo de regressão estudado teve uma performance satisfatória nos dados de teste, porém em alguns casos é possível observer claramente o *overfitting* do modelo.

<div align="center">
  <h4><b>Dados de Treino</b></h4>
</div>

<div align="center">

| **Model**                              | **R-Squared** | **MSE** | **RMSE** | **MAE** | **MAPE** |
|----------------------------------------|:-------------:|:-------:|:--------:|:-------:|:--------:|
| **Decision Tree - Regressor**          | 0.992         | 3.940   | 1.985    | 0.214   | 0.083    |
| **Random Forest Regressor**            | 0.903         | 46.271  | 6.802    | 4.856   | 2.539    |
| **Linear Regression**                  | 0.046         | 455.996 | 21.354   | 16.998  | 8.653    |
| **Linear Regression - Lasso**          | 0.007         | 474.475 | 21.782   | 17.305  | 8.737    |
| **Linear Regression - Ridge**          | 0.046         | 455.996 | 21.354   | 16.998  | 8.653    |
| **Linear Regression - ElasticNet**     | 0.008         | 474.269 | 21.778   | 17.300  | 8.732    |
| **Polynomial Regression**              | 0.094         | 432.986 | 20.808   | 16.458  | 8.351    |
| **Polynomial Regression - Lasso**      | 0.009         | 473.639 | 21.763   | 17.285  | 8.700    |
| **Polynomial Regression - Ridge**      | 0.093         | 433.475 | 20.820   | 16.472  | 8.373    |
| **Polynomial Regression - ElasticNet** | 0.013         | 471.878 | 21.723   | 17.244  | 8.679    |

</div>

<div align="center">
  <h4><b>Dados de Validação</b></h4>
</div>

<div align="center">

| **Model**                              | **R-Squared** | **MSE** | **RMSE** | **MAE** | **MAPE** |
|----------------------------------------|:-------------:|:-------:|:--------:|:-------:|:--------:|
| **Decision Tree - Regressor**          | -0.304        | 622.636 | 24.953   | 17.167  | 6.942    |
| **Random Forest Regressor**            | 0.332         | 319.078 | 17.863   | 13.029  | 7.077    |
| **Linear Regression**                  | 0.040         | 458.447 | 21.411   | 17.040  | 8.683    |
| **Linear Regression - Lasso**          | 0.008         | 473.747 | 21.766   | 17.265  | 8.696    |
| **Linear Regression - Ridge**          | 0.040         | 458.445 | 21.411   | 17.039  | 8.682    |
| **Linear Regression - ElasticNet**     | 0.008         | 473.636 | 21.763   | 17.263  | 8.694    |
| **Polynomial Regression**              | 0.066         | 445.768 | 21.113   | 16.750  | 8.548    |
| **Polynomial Regression - Lasso**      | 0.010         | 472.913 | 21.747   | 17.238  | 8.682    |
| **Polynomial Regression - Ridge**      | 0.068         | 445.184 | 21.099   | 16.739  | 8.569    |
| **Polynomial Regression - ElasticNet** | 0.013         | 471.408 | 21.712   | 17.200  | 8.675    |

</div>

<div align="center">
  <h4><b>Dados de Teste</b></h4>
</div>

<div align="center">

| **Model**                              | **R-Squared** | **MSE** | **RMSE** | **MAE** | **MAPE** |
|----------------------------------------|:-------------:|:-------:|:--------:|:-------:|:--------:|
| **Decision Tree - Regressor**          | 0.090         | 442.848 | 21.044   | 16.83   | 7.883    |
| **Random Forest Regressor**            | 0.404         | 290.205 | 17.035   | 12.243  | 6.288    |
| **Linear Regression**                  | 0,051         | 461.988 | 21.494   | 17.144  | 8.531    |
| **Linear Regression - Lasso**          | 0.051         | 461.988 | 21.494   | 17.144  | 8.531    |
| **Linear Regression - Ridge**          | 0.051         | 461.999 | 21.494   | 17.143  | 8.537    |
| **Linear Regression - ElasticNet**     | 0.051         | 461.988 | 21.494   | 17.144  | 8.531    |
| **Polynomial Regression**              | 0.091         | 442.641 | 21.039   | 16.736  | 8.277    |
| **Polynomial Regression - Lasso**      | 0.056         | 459.514 | 21.436   | 17.017  | 8.576    |
| **Polynomial Regression - Ridge**      | 0.090         | 443.041 | 21.049   | 16.744  | 8.312    |
| **Polynomial Regression - ElasticNet** | 0.059         | 457.963 | 21.400   | 16.871  | 8.451    |

</div>

### Algoritmos de Clusterização
___
Apesar da performance baixa, o que pode indicar necessidade de seleção de atributos, os dois algoritmos de clusterização encontraram o mesmo número de clusters.
</br>
<div align="center">

| **Model**                | **N Clusters** | **Average Silhouette Score** |
|--------------------------|:--------------:|:----------------------------:|
| **K-Means**              | 3              | 0.233                        |
| **Affinity Propagation** | 3              | 0.205                        |

</div>

Para esses modelos é possível observar a divisão dos clusters utilizando a técnica de *[Principal Component Analysis (PCA)](https://en.wikipedia.org/wiki/Principal_component_analysis)*.

<p align="center">
  <img alt="K-means" src="./docs/kmeans.png" width="40%">
&nbsp;&nbsp;&nbsp;
  <img alt="Affinity Propagation" src="./docs/affinitypropagation.png" width="40%">
</p>

## Conclusão
Com a observação do comportamento dos modelos para diferentes valores de hyperparâmetros nesse estudo, foi possível comprovar que esses hyperparâmetros, apesar de não causarem saltos de performance dos modelos, podem ser responsáveis diretos pela ocorrência de *overfitting* ou *underfitting*. Além disso a estratégia de separação dos dados em conjuntos de treino, validação e teste é o que possibilita a observação desses fenômenos.

Também podemos concluir que algoritmos não paramétricos tiveram melhor performancee que algoritmos paramétricos, isso pode ter acontecido por sua melhor adaptação a diferentes distribuições de dados.

## Autor
Feito com ❤️ por Elias Batista 👋🏽 Entre em contato!

<a href="https://eliasbatista.com" target="_blank"><img src="https://img.shields.io/badge/WEBSITE-689f38?style=for-the-badge&logo=About.me&logoColor=white" alt="website badge"></a>
<a href = "mailto:contato@eliasbatista.com" target="_blank"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="mail badge"></a>
<a href="https://www.linkedin.com/in/eliasbatistasouza/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="linkedin badge"></a> 
