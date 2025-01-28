# **Clustering Analysis of Dentist Office Visit Costs by Zip Code**

## **Project Overview**

This project focuses on clustering zip codes across the United States based on **dentist office visit costs**, using a dataset from the **Centers for Medicare & Medicaid Services (CMS)**. The primary goal is to identify patterns in healthcare pricing for new and established patients to support better decision-making, such as resource allocation, pricing strategies, and identifying underserved areas. 

This analysis is a step-by-step implementation of the **CRISP-DM methodology** and includes data exploration, preprocessing, modeling, and evaluation.

---

## **Table of Contents**

1. [Project Motivation](#1-project-motivation)  
2. [Dataset Overview](#2-dataset-overview)  
3. [Installation](#3-installation)  
4. [File Descriptions](#4-file-descriptions)  
5. [How to Interact with This Project](#5-how-to-interact-with-this-project)  
6. [Final Conclusion](#6-final-conclusion)  
7. [Licensing, Authors, and Acknowledgements](#7-licensing-authors-and-acknowledgements)  

---

## **1. Project Motivation**

The healthcare costs for Medicare and Medicaid patients often vary across regions. By clustering zip codes based on **Medicare pricing** and **copay costs**, this project aims to uncover patterns that can answer the following questions:

1. **Are there patterns in dental costs across different zip codes?**  
   Understanding how pricing varies can help identify low-cost or high-cost areas.
   
2. **How many meaningful clusters can we identify?**  
   Grouping zip codes into clear, meaningful clusters enables actionable segmentation.

3. **Can these clusters guide better decision-making?**  
   Clusters can inform policies for equitable Medicare reimbursements, help healthcare providers allocate resources effectively, and assist in developing cost optimization strategies.

---

## **2. Dataset Overview**

The dataset, sourced from the **Centers for Medicare & Medicaid Services (CMS)**, contains **42,966 rows** of data. It focuses on **dentist office visit costs** per zip code for both new and established patients. Below is a summary of the key features:

| **Feature Name**                                      | **Description**                                                                                          |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| `zip_code`                                            | Zip code of the dental office.                                                                           |
| `min_medicare_pricing_for_new_patient`                | Minimum Medicare price for new patients in the zip code.                                                 |
| `max_medicare_pricing_for_new_patient`                | Maximum Medicare price for new patients in the zip code.                                                 |
| `mode_medicare_pricing_for_new_patient`               | Most common Medicare price for new patients in the zip code.                                             |
| `min_copay_for_new_patient`                           | Minimum copay for new patients in the zip code.                                                          |
| `max_copay_for_new_patient`                           | Maximum copay for new patients in the zip code.                                                          |
| `mode_copay_for_new_patient`                          | Most common copay for new patients in the zip code.                                                      |
| `most_utilized_procedure_code_for_new_patient`        | Common procedure code for new patients (fixed value: `99203`).                                           |
| `min_medicare_pricing_for_established_patient`        | Minimum Medicare price for established patients in the zip code.                                         |
| `max_medicare_pricing_for_established_patient`        | Maximum Medicare price for established patients in the zip code.                                         |
| `mode_medicare_pricing_for_established_patient`       | Most common Medicare price for established patients in the zip code.                                     |
| `min_copay_for_established_patient`                   | Minimum copay for established patients in the zip code.                                                  |
| `max_copay_for_established_patient`                   | Maximum copay for established patients in the zip code.                                                  |
| `mode_copay_for_established_patient`                  | Most common copay for established patients in the zip code.                                              |
| `most_utilized_procedure_code_for_established_patient`| Common procedure code for established patients (fixed value: `99213`).                                   |

### **Dataset Source**
The data was downloaded from the official [CMS dataset page]([https://data.cms.gov/provider-data/dataset/32d8-3235]) and is titled "Dentist Office Visit Costs."

---

## **3. Installation**

To run this project, you need the following libraries installed on your system:

- **Python 3.8 or later**  
- **NumPy**  
- **Pandas**  
- **Matplotlib**  
- **Seaborn**  
- **scikit-learn**  

You can install the required libraries using the following command:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

## 4. File Descriptions

The repository contains the following key files:

- **`clustering_dentist_costs.ipynb`**: Jupyter Notebook containing the full analysis, including data exploration, preprocessing, clustering, and evaluation.
- **`Dentist.csv`**: The dataset containing zip code-level dental cost data.

---

## 5. How to Interact with This Project

To reproduce the results of this project, follow these steps to execute the notebook:

1. **Open the Jupyter Notebook**:  
   Run the `clustering_dentist_costs.ipynb` file in a Jupyter Notebook environment.

2. **Execute the Notebook Cells**:  
   Start from the top and execute each cell sequentially to follow the structured workflow, which includes:
   - Data loading and exploration.
   - Preprocessing.
   - Clustering using the KMeans algorithm.
   - Evaluation of cluster quality.
   - Visualization.

3. **Review the Outputs**:  
   The notebook includes visualizations, metrics, and a summary of the clusters.

---

## 6. Final Conclusion

### Do the clusters make sense?
Yes, the clusters reflect meaningful differences in Medicare pricing and copayments across zip codes. The segmentation highlights clear patterns in healthcare costs.

### What defines each cluster?
- **Cluster 0**: Economic zones with consistently low Medicare pricing and copayments.
- **Cluster 1**: Intermediate zones, representing mid-range costs likely found in suburban areas.
- **Cluster 2**: High-cost zones, possibly representing premium healthcare regions.
- **Cluster 3**: Zones with low costs but slightly different characteristics compared to Cluster 0.

### Is the model robust?
Yes, the model demonstrates consistency in both the training and testing datasets. The **Silhouette Scores** (~0.60 for both) indicate that the clusters are well-defined and generalizable.

### What relevant patterns can we leverage?
The identified clusters can be applied to:
1. Segment postal codes for targeted pricing strategies.
2. Guide resource allocation in healthcare planning.
3. Conduct deeper analysis on cost differences across regions to inform Medicare reimbursement policies.

---

## 7. Licensing, Authors, and Acknowledgements

### **Licensing**
This project is for educational purposes and is not intended for commercial use. The dataset is sourced from **CMS**, a public U.S. government agency.

### **Author**
This project was completed by **[Roberto Ruiz]** as part of my Data Scientist Program Nanodegree in Audacity.

### **Acknowledgements**
- Thanks to the **Centers for Medicare & Medicaid Services (CMS)** for providing the dataset.  
- Special thanks to the **Udacity Data Scientist Nanodegree program**, which inspired the structure and documentation style of this project.

