# Analysis and Prediction of High-Impact Anomalous Bushfire Events in Victoria
## Project Overview
This project presents a machine learning framework for the identification of rare, high-impact bushfire events in Victoria, Australia. The core objective is to move beyond traditional, seasonal fire management by developing a system that can accurately detect dangerous fires that occur outside of the typical high-risk summer period. This is particularly challenging due to the infrequent nature of these "anomalous" events, which are often difficult to distinguish from common occurrences like prescribed burns.

The final model, a supervised Random Forest classifier, was trained on a comprehensive dataset integrating satellite-detected fire locations from the NASA FIRMS portal with meteorological data from seven weather stations across Victoria. This approach addresses the problem of extreme data imbalance, where anomalous fires made up only 0.43% of the dataset. The model achieved an F1-Score of 0.857, demonstrating its effectiveness in a task where specialized unsupervised anomaly detection models failed.

## Research Methodology
The project followed a systematic five-phase approach:

### Data Acquisition and Preprocessing: 
Raw fire data from NASA FIRMS and daily meteorological data from the Open-Meteo API were collected and filtered.

### Exploratory Data Analysis (EDA): 
A detailed analysis was conducted to uncover patterns and refine the research question. This phase revealed a significant number of fires were due to prescribed burning, which led to a more specific focus on high-intensity fires in low-risk seasons.

### Feature Engineering and Data Integration: 
New features, such as temperature range, were engineered from the raw data. Fire incidents were then merged with the nearest weather station data to create a single, unified analytical dataset.

### Anomaly Definition and Dataset Preparation: 
Anomalous fires were precisely defined as high-intensity fires (top 10% of Fire Radiative Power) occurring during the low-risk season (May-August). This created a final dataset with a significant class imbalance that required specific handling.

### Model Training and Evaluation: 
A suite of supervised and unsupervised models was trained and evaluated. Techniques like class weighting were applied to the supervised models to address the data imbalance. The F1-Score was used as the primary metric for performance evaluation.

## Project Contents and Usage
The project repository contains all the necessary components to replicate the analysis and findings:

```seasonal_analysis_investigation.py```: The main script for the project, containing the full methodology from data processing to model evaluation. This script is located in the GitHub repository.

Datasets: The required fire and weather data are included in the repository.

Jupyter Notebooks: These notebooks contain all the necessary commands to install the required packages and run the analysis. They will automatically generate the processed parquet files and perform the analysis, provided the raw datasets are in the same folder.

Instructions to Run
Ensure you have Python ```3.11.7``` installed on your system.

Clone this repository to your local machine.

Navigate to the project directory.

Open the Jupyter notebook. All necessary packages will be installed and the analysis will run automatically from the notebook cells. The notebooks are designed to process the raw datasets, create the required parquet files, and perform the full analysis.

References
Please refer to the ```milestone_d.docx``` report for the full list of references.
