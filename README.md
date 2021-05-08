## Pubmed Article Search REST API

Language: Java

Skillset: Springboot, microservices, file I/O, Lucene

[lazrichardson/article-database](https://github.com/lazrichardson/article-database)

**Use Case**

My application is a REST API. It takes local XML files downloaded from Pubmed and parses them using the SAX parser. It takes the article title and dates from those files and loads them into a local in-memory database, as well as a Lucene database. Finally, it provides an endpoint for searching for those articles utilizing Spring Boot. The endpoint supports searching by a combination of keyword and start to end dates.

**Design goals**

- Make the project extensible
- High readability of the data load + parsing process
- Easy to implement different searching algorithms
- Loose coupling between databases and parsing

### **Patterns Utilized**

**API Gateway / Microservices**

This pattern determines the overall structure of the application. My application provides the client with an endpoint to call on an aggregation of microservices from a single location, which is through the HTML query. The user doesn't have to call on each microservice on its own, even though many are used to return the data, in this case the search results, to the client. This allows the implementation of the microservices to change without the client needing to know.

**Pipeline**

I used this pattern to provide the behaviour for the XML parsing process in my application. The Pipeline allows for the processing of data in stages, with each step feeding directly to the next. This pattern is ideal for data processing because it greatly increases the modularity of the process, allowing for enhanced troubleshooting by enabling enhanced readability of complex operations. This pattern also supports the use of the Single Responsibility Principle (SRP)

**Strategy**

The strategy pattern is used in this application to encapsulate different searching behaviours. Each database provides the context for the search strategy.

**Facade**

The database classes act as a facade for additional search complexity where search items and indexes are passed to the search methods, which also utilize the Strategy pattern.

## **Data Science Projects**

This repository highlights example projects for datascience.

[lazrichardson/DataScienceExampleProjects](https://github.com/lazrichardson/DataScienceExampleProjects)

### **Bag of Words and Latent Semantic Analysis**

This project implements a bag of words and topic clustering using Latent Semantic Analysis

This project uses the IndieGogo Dataset ([https://webrobots.io/indiegogo-dataset/](https://webrobots.io/indiegogo-dataset/)) to download at least 5 files. It takes the “title” for each project in the dataset.

Then, the article titles are put into a “bag of words” format. Finally, Latent Semantic Analysis (LSA) is used to cluser them into related topics.

### **Dimensionality Reduction**

This project is focused on dimensionality reduction of textual data.

- This project downloads at least 200 Pubmed articles. 100 include the term “obesity”, and the other 100 include the term “cancer”.
- Their textual corpus is analyzed to feed them into a dimensionality reduction method.
- Finally, Principal Component Analysis (PCA), T-distributed stochastic neighbor embedding (tSNE), and Uniform Manifold Approximation and Projection for Dimension Reduction (UMAP) algorithms are applied to the dataset to visualize the

### **Graph Analysis**

This project explores different approaches to graph analysis.

- Dijkstra's shortest path visualized on a graph.
- Prim's, and Kruskal's minimum spanning tree algorithms to find the MST between two arbitrary nodes
- Visualization of Page rank and HITS algorithm to order the graph nodes based on their importance
- Visualization of the Louvain and Leiden algorithms for community detection

### **Sentiment Analysis**

This project collects tweets about soccer to analyze their sentiment, comparing results of Afinn and FastText.

- Search, clean, and load the tweets using the Twitter API
- Calculate sentiments using Afinn
- Train a FastText model
- Find sentiments using FastText model

### **Distribution Analysis and Testing**

This project is focused on exploring different testing methods using the IndieGogo dataset

It demonstrates:

- Testing for Gaussian distributions using Q-Q plots, and the Shapiro Wilk test
- Parametric testing using the Welch Two Sample t-test
- Non-Parametric testing using Two-sample Kolmogorov-Smirnov test and Wilcoxon rank sum test with continuity correction
- Calculation of effect size to quantify the magnitude of differences using Cohen's D
- Correlation Coefficient testing (Pearson, Spearman, KendallTau)

# Meme Generator

This project is an example bootstrap web application.

To see the live app, navigate to: [https://lazrichardson.github.io/MemeGenerator/](https://lazrichardson.github.io/MemeGenerator/)

[lazrichardson/MemeGenerator](https://github.com/lazrichardson/MemeGenerator)

### **Key details**

- All local - no back end to store images
- Print / share your image directly from the app
- Ability to upload your own image
- Provide multiple template memes for users to choose from

## Processor Pipeline Simulation

Language: Java

Skillset: Bit Shifting, Pipelined Datapath

Description: Simulates a pipelined datapath for selected machine language instructions 

[lazrichardson/PipelineSim](https://github.com/lazrichardson/PipelineSim/tree/master/src)

## Shopping List Android App

Language: Java

Skillset: Android Application Development

Description: The user can input a list of items and the application will purchase items for the user based on their input budget.

[lazrichardson/Shopping-List-Final-Project](https://github.com/lazrichardson/Shopping-List-Final-Project)
