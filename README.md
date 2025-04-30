# Amazon Co-Purchase Network Analysis

This project analyzes the Amazon co-purchase network using metadata from the Amazon product catalog. The goal is to preprocess raw data, build a graph representation of product co-purchases, and perform community detection using the Louvain method to uncover product clusters.

## 📁 Project Structure

- `amazon-meta.txt.gz`: Raw dataset containing product metadata, reviews, and co-purchase links.
- `BigDataAmazon.ipynb`: Main Colab notebook for preprocessing, network analysis, and visualization.
- `products_cleaned.csv`, `categories_cleaned.csv`, `reviews_cleaned.csv`: Cleaned product, category, and review data.
- `edges.csv`: Weighted edge list for graph construction.
- `products_enriched.csv`, `categories_expanded.csv`, `reviews_processed.csv`: Further enriched datasets.
  
## 🔧 Requirements

Install the following Python packages before running the notebook:

```bash
pip install python-louvain networkx matplotlib igraph textblob torch-geometric plotly
```

## 🚀 Features

- **Data Preprocessing**:
  - Parses the compressed `amazon-meta.txt.gz` file.
  - Extracts valid product, category, and review records.
  - Filters out unknown or incomplete entries.

- **Sentiment Analysis**:
  - Computes sentiment polarity for reviews using TextBlob.

- **Graph Construction**:
  - Builds a directed product co-purchase network using NetworkX.
  - Maps product ASINs to node indices for graph modeling.

- **Community Detection**:
  - Detects product clusters using the Louvain method.
  - Visualizes graph communities with interactive layouts.

- **Optional GNN Integration**:
  - Code structure supports further integration with PyTorch Geometric for deep learning-based link prediction.

## 📊 Visualization

The notebook provides various visualizations using `matplotlib` and `plotly`, including:

- Community structure graphs
- Product co-purchase network layouts

## 🧠 Future Extensions

- Implement Graph Autoencoder (GAE) for link prediction.
- Add node feature engineering using product categories or sentiment embeddings.
- Support for scalable graph analysis with distributed tools.
