# Stock Price Forecast

### Portfolio Optimizer anallyses cryptocurrencies by their performance in different time periods by utilizing the scikit-learn library. The data is first normalized with the help of StandardScaler module. Then, K-Means model is applied to both the normalized data, as well as to the optimized with the Principal Component Analysis dataset, to generate the clusters of cryptocurrencies based on their performance. The results are also vizually presented and compared, allowing for further in-depth analysis.

---

![ecommerce](Images/online.jpg)

---

## Table of contents

1. [Technologies](#technologies)
2. [Installation Guide](#installation-guide)
3. [Usage](#usage)
4. [Contributors](#contributors)
5. [License](#license)

---

## Technologies

`Python 3.9`

`Jupyter lab`

_Prerequisites_

1. `Pandas` is a Python package that provides fast, flexible, and expressive data structures designed to make working with large sets of data easy and intuitive.

   - [pandas](https://github.com/pandas-dev/pandas) - for the documentation, installation guide and dependencies.

2. `PyViz` is a Python visualization package that provides a single platform for accessing multiple visualization libraries. One of these libraries is hvPlot. <br/>

   - [PyViz ](https://pyviz.org/) - for guidance on how to start visualization, interactive visualization, styles and layouts customazation.
   - [hvPlot ](https://hvplot.holoviz.org/) is a visualization library that is designed to work with Pandas DataFrames and that we can use to create interactive plots for our data.<br/>

3. `Scikit-learn` is a simple and efficient tools for predictive data analysis. It is built on NumPy, SciPy, and matplotlib.

   - [scikit-learn ](https://scikit-learn.org/stable/) - for information on the library, its features and installation instructions.<br/>

---

## Installation Guide

Jupyter lab is a preferred software to work with Risk Return Analysis application.<br/> Jupyter lab is a part of the **[anaconda](https://www.anaconda.com/)** distribution package and therefore it is recommended to download **anaconda** first.<br/> Once dowloaded, run the following command in your terminal to lauch Jupyter lab:

```python
jupyter lab
```

Before using the application first install the following dependencies by using your terminal:

To install pandas run:

```python
#  PuPi
pip install pandas
```

```python
# or conda
conda install pandas
```

To install PyViz, in Terminal run:

```python
# conda
conda install -c pyviz hvplot
```

Confirm the installation of all the PyViz packages by running the following commands in Terminal type:

```python
 conda list hvplot
```

To install scikit library, in Terminal run:

```python
# PuPi
pip install -U scikit-learn
```

Confirm the installation of the scikit library by running the following commands in Terminal type:

```python
 conda list scikit-learn
```

---

## Usage

> Application summary<br/>

Portoflio Optimizer takes us through the necseesary steps to perform data clustering, including data normalization, selecting an optimal k for the K-means algorithm, clustering optimization with Principal Component Analysis <br/>
The tool consists of two parts: <br/>
a) Clustering with K-mean by using the original scaled data<br/>
b) Cluster optimization with Principal Componenet Analysis. <br/>
The results of (a) and (b) are compared and the conclusion is drawn at the end of the application.<br/>

**_Clustering with K-mean by using the original scaled data_**<br/>

- The analyzis begings by loading cryptocurrencies performance over different time periods:<br/>
  ![crypto_initial](Images/initial_df.png)<br/>
- Next, we use the `StandardScaler` module from scikit-learn to normalize the CSV file data. The `fit_transform` function from the StandardScaler` module is utilized, resulting in:<br/>
  ![normalized_data](Images/scaled_segmented_df.PNG)<br/>
- We use the elbow technique to find the optimal k value for the K-means algorithm:<br/>
  ![normalized_elbow](Images/elbow_scaled.png)<br/>
- Once an optimal k-value is chosen, K-Means model is applied to produce clusters:<br/>
  ![scatter_plot_normalized](Images/scatter_scaled.png)<br/>

**_Clusters optimization with Principal Component Analysis (PCA)_**<br/>

- A new dataset is created by applying PCA model and chosing three Principal Components:<br/>
  ![pca_data](Images/PCA_segmented_dfPNG.PNG)<br/>
- The elbow technique to find the optimal k value for the K-means model is applied:<br/>
  ![elbow_pca](Images/elbow_pca.png)<br/>
- And again, once the optimal k-value is chosen, K-Means model is applied to the new PCA dataset to produce clusters:<br/>
  ![pca_clusters](Images/scatter_pca.png)<br/>

**_Comparision_**<br/>

- We finalyze by comparing the elbow curves and the clusters generated with and without PCA model applied to our dataset and draw the conclusion at the end of the tool.<br/>

> Getting started<br/>

- To use Portoflio Optimizer first clone the repository to your PC.<br/>
- Open `Jupyter lab` as per the instructions in the [Installation Guide](#installation-guide) to run the application.<br/>

---

## Contributors

Contact Details:

Boris Dudkin:

- [Email](boris.dudkin@gmail.com)
- [LinkedIn](www.linkedin.com/in/Boris-Dudkin)

---

## License

MIT

---
