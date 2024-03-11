# COVID-19 Literature Clustering

This project aims to cluster COVID-19 related articles using unsupervised machine learning and data mining techniques. The main objectives are:

- To group similar articles based on their content and keywords
- To visualize the clusters in a lower-dimensional space using t-SNE[^5^][5]
- To perform topic modeling using Latent Dirichlet Allocation (LDA) to identify the main topics within each cluster
- To implement a document suggestion system that can return similar articles based on a given query

## Dataset

The dataset used for this project is the [CORD-19](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge) dataset, which consists of over 500,000 articles in several languages, mainly in English, containing information about COVID-19, SARS-CoV-2, and other related coronaviruses[^6^][6]. This dataset was created by the White House and a consortium of leading research groups to support the scientific and medical research communities in tackling the COVID-19 pandemic.

## Methods

The following methods and algorithms were used in this project:

- Natural Language Processing (NLP) to parse, preprocess, and vectorize the text from each document using scispacy and Term Frequency-Inverse Document Frequency (TF-IDF)
- Principal Component Analysis (PCA) to reduce the dimensionality of the feature vectors while preserving 95% of the original variance
- K-Means, Spectral Clustering, and Gaussian Mixture Models (GMM) to cluster the documents based on their similarity
- t-SNE to project the high-dimensional feature vectors to a two-dimensional space for visualization[^7^][7]
- LDA to extract the keywords and topics from each cluster[^8^][8]
- Cosine similarity, Euclidean distance, and Jensen Shannon divergence to measure the similarity between documents and return the most similar ones based on a given query[^9^][9]

## Results

The results of the clustering and topic modeling are shown in the following figures and tables:

![TSNE_kmeans](https://github.com/pareekshitreddy/COVID-19-Literature-Clustering/assets/91700444/106e04f4-7735-4769-8f98-a92775375b6f)[^8^][8]

![T-SNE with GMM Labels]([tsne_gmm.png](https://github.com/pareekshitreddy/COVID-19-Literature-Clustering/assets/91700444/bfb14f9e-5c8d-4536-9177-712130c7dfa1))[^8^][8]

![First Word Cloud]([wordcloud1.png](https://github.com/pareekshitreddy/COVID-19-Literature-Clustering/assets/91700444/9abec0a3-b2ed-442c-9af1-b92a97554d9c))[^8^][8]

![Second Word Cloud]([wordcloud2.png](https://github.com/pareekshitreddy/COVID-19-Literature-Clustering/assets/91700444/6a7265da-1677-4fc7-bf92-d3f301544aeb))[^8^][8]

| Metrics | K-Means | Spectral Clustering | GMM |
|---------|---------|---------------------|-----|
| Silhouette Score | 0.0727 | 0.1129 | 0.1484 |[^1^][1][^2^][2][^3^][3]
| Davies Bouldin Score | 1.3607 | 1.3288 | 1.2860 |

The document suggestion system can return a list of similar documents based on a given document, as shown in the following example:

![Similar Documents](similar_docs.png)

## Conclusion and Future Work

In this project, we applied various unsupervised machine learning and data mining techniques to cluster and analyze the COVID-19 literature. We were able to group the articles into meaningful clusters and identify the main topics and keywords within each cluster. We also implemented a document suggestion system that can help researchers find relevant and similar articles based on their queries.

Some possible directions for future work are:

- To use Word2Vec to generate embeddings for the documents instead of TF-IDF[^12^][12]
- To implement model-based overlapping clustering to account for the overlap between clusters
- To explore other evaluation methods for clustering and topic modeling
- To improve the user interface and functionality of the document suggestion system
