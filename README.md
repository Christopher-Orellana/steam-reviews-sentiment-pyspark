# Steam Reviews Predictive Modeling Pipeline (PySpark + GCP)

This project presents a scalable data pipeline for predictive modeling on a 47GB Steam reviews dataset using PySpark and Google Cloud Dataproc. For a deeper look at methodology, design decisions, and pipeline architecture, refer to the included PDF milestone report: **`milestone_report.pdf`**.

## Objective

To construct a robust and modular big data pipeline capable of:
- Loading and processing raw data from Google Cloud Storage (GCS)
- Performing distributed exploratory analysis on review data
- Cleaning and preparing the data for modeling
- Engineering features to support a predictive model

## Dataset

**Steam Reviews Dataset (47GB CSV)**  

Includes:
- Review text  
- Review score (binary sentiment)  
- Timestamps  
- Product and user metadata  

Due to size, the dataset is stored on GCS and processed on a Dataproc cluster using PySpark for distributed compute power.

## Tools and Technologies

- PySpark (Spark SQL, DataFrame API)
- Google Cloud Storage (GCS)
- Google Cloud Dataproc
- JupyterLab
- Git & GitHub

## Notebooks

| Notebook File | Description |
|---------------|-------------|
| `pyspark_steamReview_EDA_gitr.ipynb` 			| Performs distributed exploratory data analysis on the full dataset |
| `pyspark_steamReview_cleaned_gitr.ipynb` 		| Applies schema fixes, text normalization, null filtering, and prepares structured data |
| `pyspark_steamReview_feature_engineering_gitr.ipynb` 	| Engineers features to support predictive modeling (e.g., review length, user flags, text metadata) |

## Project Structure

```
steam-reviews-predictive-pipeline/
│
├── notebooks/                        # EDA, Cleaning, Feature Engineering
│   ├── pyspark_steamReview_EDA_gitr.ipynb
│   ├── pyspark_steamReview_cleaned_gitr.ipynb
│   └── pyspark_steamReview_feature_engineering_gitr.ipynb
│
├── data/                             # Cleaned or sampled subsets
├── milestone_report.pdf              # Full written report on pipeline design and findings
├── requirements.txt                  # Package dependencies
├── .gitignore                        # Files/folders to exclude from version control
└── README.md                         # Project overview and documentation
```

## Work Summary

- Ingested and analyzed a 47GB dataset using Spark on Dataproc  
- Built a distributed data pipeline for EDA, cleaning, and transformation  
- Engineered predictive features based on textual and metadata fields  
- Structured the dataset for downstream model training

## Next Steps
 
- Experiment with more interactions and transformations of features to better fit the data
- Optimize pipelines for repeatability and deployment across cloud systems

## Author

**Christopher Orellana**  
M.S. Candidate, Data Analytics  
Baruch College  
