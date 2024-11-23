McDonald's Customer Segmentation Analysis
Overview
This project performs customer segmentation on McDonald's survey data to identify distinct customer groups based on their preferences and behaviors. The analysis leverages clustering algorithms, dimensionality reduction techniques, and Gaussian Mixture Models (GMM) to extract meaningful insights from the data. Visualization and profiling of segments provide an in-depth understanding of customer characteristics.

Key Features
Preprocessing:

Handles binary responses (e.g., "Yes"/"No") by converting them into numeric representations.
Encodes categorical features like Gender and VisitFrequency for clustering compatibility.
Dimensionality Reduction:

Principal Component Analysis (PCA) is applied for visualizing data in 2D.
Explained variance and principal component loadings are computed.
Clustering Algorithms:

KMeans Clustering: Used to group customers into segments.
Gaussian Mixture Model (GMM): Provides probabilistic clustering and enables information criteria (AIC, BIC) evaluation.
Hierarchical Clustering: Applied on both customer attributes and survey variables.
Stability Evaluation:

Scree plot (Elbow Method) determines the optimal number of clusters.
Adjusted Rand Index (ARI) measures the stability of cluster solutions across bootstrap samples.
Visualization:

PCA scatter plots for visualizing cluster separation.
Dendrograms for hierarchical clustering.
Boxplots and countplots for profiling clusters based on survey responses.
Segment Profiling:

Analyzes cluster-specific averages for numerical features.
Distribution plots highlight differences in customer preferences.
Dataset
The dataset used in this analysis contains survey responses from McDonald's customers. Key features include demographic information, visit frequency, and ratings for various attributes of the McDonald's experience.

Getting Started
Prerequisites
Ensure the following Python libraries are installed:

pandas
numpy
scikit-learn
matplotlib
seaborn
scipy
You can install the dependencies using:

bash
Copy code
pip install pandas numpy scikit-learn matplotlib seaborn scipy
Usage
Clone this repository:
bash
Copy code
git clone https://github.com/<your-username>/mcdonalds-segmentation.git
Navigate to the project directory:
bash
Copy code
cd mcdonalds-segmentation
Run the script:
bash
Copy code
python main.py
File Structure
main.py: The primary script containing the analysis pipeline.
mcdonalds.csv: The dataset used for analysis (not included, ensure you upload your dataset here).
README.md: Project documentation.
Outputs
The analysis produces the following outputs:

PCA plots showing data projections and loadings.
Scree plots and silhouette scores for cluster evaluation.
Stability boxplots for evaluating clustering robustness.
Segment-specific profiling visualizations (e.g., boxplots, bar charts).
Cross-tabulations for comparing GMM and KMeans solutions.
Key Insights
This analysis enables businesses to:

Identify distinct customer segments and their preferences.
Understand the stability of segmentation solutions.
Optimize marketing strategies tailored to each customer group.
Future Enhancements
Implement automated feature selection for profiling segments.
Integrate unsupervised feature learning (e.g., t-SNE or UMAP) for advanced visualization.
Compare additional clustering algorithms, such as DBSCAN or Agglomerative Clustering.
License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For questions or feedback, please reach out at [your email/contact info].
