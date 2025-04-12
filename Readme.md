# Customer Segmentation of an e-commerce website

This project focuses on customer segmentation using behavioral and personal data to identify distinct customer groups and analyze their characteristics. Additionally, it estimates the maintenance time for the clustering model, determining when the model should be retrained based on the stability of customer segments over time.

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Data](#data)
- [Methodology](#methodology)
- [Results](#results)
- [How to Run](#how-to-run)
- [Dependencies](#dependencies)

## Overview
Customer segmentation is a critical task for businesses to understand their customer base, tailor marketing strategies, and improve customer satisfaction. This project employs clustering techniques to segment customers based on Recency, Frequency, Monetary value, and additional features such as Review Score and Total Items purchased. 

The project also includes a maintenance time estimation module that uses the Adjusted Rand Index (ARI) to evaluate the stability of clusters over time and determine when the clustering model should be retrained.

## Project Structure
The project is organized into three main notebooks:
1. **[1_EDA.ipynb](1_EDA.ipynb)**: Exploratory Data Analysis (EDA) to understand the dataset and prepare it for clustering.
2. **[2_segmentation.ipynb](2_segmentation.ipynb)**: Customer segmentation using KMeans clustering and analysis of different segmentation strategies (RFM, RFMS, RFMST, RFMSA).
3. **[3_maintenance_time_estimation.ipynb](3_maintenance_time_estimation.ipynb)**: Maintenance time estimation to determine when the clustering model should be retrained based on segment stability.

## Data
The project uses customer data located on Kaggle : https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce.
<br>
This is a Brazilian ecommerce public dataset of orders made at [Olist Store](http://www.olist.com/). The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil.
<br>
This is real commercial data, it has been anonymised, and references to the companies and partners in the review text have been replaced with the names of Game of Thrones great houses.

## Methodology
1. **Exploratory Data Analysis**:
   - Visualize distributions of features.
   - Identify correlations and patterns in the data.

2. **Customer Segmentation**:
   - Use KMeans clustering to segment customers based on RFM and extended features (RFMS, RFMST, RFMSA).
   - Evaluate the optimal number of clusters using the Elbow Method and Calinski-Harabasz Index.
   - Analyze cluster characteristics using box plots, distribution plots, and PCA visualizations.

3. **Maintenance Time Estimation**:
   - Compare cluster assignments over time using the Adjusted Rand Index (ARI).
   - Identify the threshold (e.g., ARI < 0.8) to determine when the clustering model should be retrained.

## Results
- **Segmentation**:
  - Identified distinct customer groups, such as high-spending customers, frequent buyers, and unsatisfied customers.
  - Extended features (e.g., Review Score, Total Items) improved the segmentation quality.

- **Maintenance Time Estimation**:
  - Demonstrated how ARI can be used to monitor cluster stability and determine the optimal retraining interval for the clustering model.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/customer-segmentation.git
   cd customer-segmentation

2. Install dependencies (see [Dependencies](#dependencies)).

3. Run the notebooks in the following order:
   - 1_EDA.ipynb
   - 2_segmentation_analysis.ipynb
   - 3_maintenance_time_estimation.ipynb

4. Ensure the required data files (downloaded from [Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)) are placed in the `data/` directory.

## Dependencies
The project requires the following Python libraries:
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- yellowbrick

Install the dependencies using:
```
pip install -r requirements.txt
```

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
Special thanks to the contributors and the open-source community for providing the tools and libraries used in this project.
