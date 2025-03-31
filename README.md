# Cancer Patient Data Analysis
## Project Overview
This project involves performing exploratory data analysis (EDA), data cleaning, and visualization on a cancer patient dataset stored in a CSV file named "cancer_patient_data_sets.csv." The goal is to understand the distribution of cancer types, patient demographics, and other relevant factors.

## Data Sources
The dataset includes information such as:

- Patient Demographics: Age, gender, location.
- Cancer Types: Malignant or benign classifications.
- Clinical Features: Tumor size, cell characteristics, treatment outcomes.

## Data Preparation
Before analysis, the following steps were performed:

- Data Cleaning:
- Removed duplicates and unnecessary fields.
- Handled missing values (e.g., imputing means for continuous variables).
- Standardized date formats for consistency.

## Data Transformation:

- Categorized continuous variables into bins for easier visualization.
- Converted categorical variables into numerical formats for analysis.

## Exploratory Data Analysis (EDA)
To understand the dataset's structure and trends, the following EDA steps were conducted:

python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

### Load the dataset
data = pd.read_csv('cancer_patient_data_sets.csv')

#### Explore the first few rows
print(data.head())

#### Check for missing values
print(data.isnull().sum())

#### Visualize distribution of cancer types
sns.countplot(data['cancer_type'])
plt.show()

#### Plot age distribution
sns.histplot(data['age'], kde=True)
plt.show()
Data Visualization
The following visualizations were created to highlight key insights:

- Bar Charts: Compared the frequency of different cancer types.
- Histograms: Showed the distribution of patient ages and tumor sizes.
- Scatter Plots: Examined correlations between clinical features 

### Visualize age vs. tumor size
sns.scatterplot(x='age', y='tumor_size', data=data)
plt.show()

### Plot survival rates by cancer type
sns.barplot(x='cancer_type', y='survival_rate', data=data)
plt.show()

## Key Insights
Cancer Type Distribution:

- Identified most common cancer types among patients.
- Determined the proportion of malignant vs. benign cases.

Patient Demographics:

- Found age ranges with the highest incidence of cancer.
- Analyzed gender distribution among cancer patients.

Clinical Features:

- Examined correlations between tumor size and treatment outcomes.

- Identified factors influencing survival rates.

## Project Structure
text
├── data/
│   ├── cancer_patient_data_sets.csv
└── scripts/
    ├── data_cleaning.py
    ├── eda.py
    └── visualization.py
└── insights/
    ├── cancer_type_distribution.md
    ├── patient_demographics.md
    └── clinical_features.md
## Technologies Used
- Python: For data manipulation and analysis.
- Pandas: For data handling and cleaning.
- Matplotlib/Seaborn: For data visualization.
