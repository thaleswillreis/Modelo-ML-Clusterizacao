# **Projeto de Clusterização de Clientes** *(Setor de Energia Elétrica)*

Projeto destinado a criação, teste e avaliação de um exemplo de modelo de Machine Learning de clusterização, utilizando dados de clientes consumidores de energia elétrica de uma determinada fornecedora de energia. Nesse projeto, o foco foi a utilização do algoritmo **KMeans**, mas também foram utilizados para fins de comparação os algoritmos **AgglomerativeClustering**, **DBSCAN** - (Density-Based Spatial Clustering of Applications with Noise) e **Gaussian Mixture Model** (GMM).

<br>

## Fases do projeto

1. Análise exploratória dos dados

   * Verificação das características gerais dos dados;
   * Verificação de dados faltantes;
   * Verificação de dados inconsistentes;
   * Engenharia de atributos.

<br>

2. Transformação dos dados

   * Tratamento de dados nulos ou incorretos;
   * Exclusão de dados irrelevantes;
   * Separação dos dados de treinamento e de teste;
   * Normalização e/ou Padronização dos dados.

<br>

3. Criação, Teste e Avaliação dos Modelos de Regressão Linear

   * Criação dos modelos
     1 - Modelo KMeans;
     2 - Modelo AgglomerativeClustering;
     3 - Modelo DBSCAN - (Density-Based Spatial Clustering of Applications with Noise);
     4 - Modelo GMM - (Gaussian Mixture Model).
   * Treinamento dos modelos;
   * Teste dos modelos;
   * Avaliação dos modelos.

<br>

## Tecnologias Utilizadas

Esse projeto foi executado utilizando a linguagem Python no formato Jupyter Notebook. Foram utilizadas as bibliotecas Pandas (Carregamento, Limpeza e Análise dos Dados), Matplotlib (Visualização de dados e geração de gráficos), Sklearn (Criação, treinamento e avaliação dos modelos de Machine Learning), Git (Versionamento de código) e a IDE escolhida foi o Visual Studio Code, rodando em um Debian Linux.

**Links relacionados:**

* [Debian Linux](https://www.debian.org/index.pt.html)
* [VSCode](https://code.visualstudio.com/)
* [Python](https://www.python.org/)
* [Jupyter](https://jupyter.org/)
* [NumPy](https://numpy.org/)
* [Pandas](https://pandas.pydata.org/)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/#)
* [Sklearn](https://scikit-learn.org/stable/)
* [Git](https://git-scm.com/)

### Dependências e Versões Necessárias

Os softwares e bibliotecas utilizados no projetos tinham a seguintes versões:

* Python - Versão: 3.11.5
* NumPy - Versão: 1.26.4
* Pandas - Versão: 2.2.1
* Matplotlib - Versão: 3.8.3 (matplotlib-inline: 0.1.6)
* Seaborn - Versão: 0.13.2
* Scikit-learn - Versão: 1.4.1

**Obs:** para mais detalhes consulte o aquivo **"requirements.txt"**

## Problemas enfrentados

O código poderá enfrentar problemas ao ser executado utilizando versões diferentes de linguagem e bibliotecas. Certifique-se de que as versões listadas no item "Dependências e Versões Necessárias" estão corretamente instaladas.

Caso já exista um ambiente de desenvolvimento com versões diferentes em uso na máquina utilizada, uma boa alternativa seria a criação de uma ambiente virtual de desenvolvimento. Em caso de dúvida, segue o link da documentação.
[Ambientes virtuais e pacotes](https://docs.python.org/pt-br/3/tutorial/venv.html)

## Resultados Obtidos e Métricas de Avaliação:

#### **Modelo_v1:**

* **Algoritmo:** KMeans
* **Clusters:** 7
* **Métricas:**

  * **silhouette score:** 0.8617262776483926

#### **Modelo_v1:**

* **Algoritmo:** KMeans
* **Clusters:** 7
* **Métricas:**

  * **silhouette score:** 0.8617262776483926

#### **Modelo_v2:**

* **Algoritmo:** KMeans
* **Clusters:** 9
* **Métricas:**

  * **silhouette score:** 0.8087643953544675

#### **Modelo_v3:**

* **Algoritmo:** KMeans
* **Clusters:** 6
* **Métricas:**

  * **silhouette score:** 0.8380044143347933

#### **Modelo_v4:**

* **Algoritmo:** KMeans
* **Clusters:** 5
* **Métricas:**

  * **silhouette score:** 0.7322773427162191

#### **Modelo_v5:**

* **Algoritmo:** KMeans
* **Clusters:** 4
* **Métricas:**

  * **silhouette score:** 0.8578440511109866

#### **Modelo de comparação 1:**

* **Algoritmo:** AgglomerativeClustering
* **Clusters:** 7

#### **Modelo de comparação 2:**

* **Algoritmo:** DBSCAN
* Parâmetros:
  * **eps:** 0.03
  * **min samples:** 20
* **Clusters:** 5
* **Ruído:** 435 de 40985

#### **Modelo de comparação 3:**

* **Algoritmo:** GaussianMixture
* **Clusters:** 7

## **Resultados:**

Para este conjunto de dados, o modelo utilizando o algoritmo KMenas com 7 clusters e dados padronizados, foi o que pareceu abstrair melhor as características do conjunto dos dados. Os algoritmos utilizados para verificação, conseguiram replicar o resultado rasoavelmente bem, sendo que os modelos usando AgglomerativeClustering e DBSCAN, foram utilizados no mesmo conjunto de dados do KMeans, com cerca de 40 mil registros, já o algoritmo GaussianMixture, por se tratar de um algoritmo bem menos custoso computacionalmente, foi utilizado com o conjunto total dos dados contendo um pouco mais de 2 milhões de registros.

Nesse sentido, o que se observou foi que, o modelo GaussianMixture conseguiu abstrair características dos dados até certo ponto semelhantes aos rotulados pelo KMeans. Já o DBSCAN, apesar de criar clusters ligeiramente parecidos, entre todos os ajustes de hiperparâmetros testados, acabou rotulando, no seu melhor resultado, 1.06% dos dados como ruído, o que apesar de não representar algo inaceitável, pode inviabilizar o uso desse algoritmo para determinados tipos de problemas com esse conjunto de dados.
