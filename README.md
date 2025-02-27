# 4660Project

Gene Expression Signatures of Survival in Ovarian Serous Cystadenocarcinoma 

Author: Faloseyi Oluwatomilayo 

Project Track: Mad data scientist level 

 
Background: As someone who has seen many women around me suffer from breast cancer, I find this research deeply relevant. Understanding what happens inside a patient’s body at the molecular level can provide crucial insights into cancer progression and treatment. Since we have primarily studied breast cancer in class, I wanted to explore another significant cancer affecting women— Ovarian Serous Cystadenocarcinoma (OSC). OSC is the most common and aggressive form of ovarian cancer, often diagnosed at an advanced stage with poor survival rates. Identifying key genes linked to survival could improve early detection, prognosis, and treatment strategies. By analysing gene expression patterns, the aim is to uncover potential genetic biomarkers and gain insights into OSC’s biological mechanisms. 

Research Hypothesis: For this study we hypothesize that mRNA expression levels of key genes are significantly associated with survival classification (high vs. low survival) in patients with OSC. 

Data Sketch: The dataset consists of gene expression and clinical data for patients with OSC from The Cancer Genome Atlas. The clinical data includes information on patient demographics, tumour characteristics, and survival outcomes. This dataset allows us to explore the relationship between gene expression patterns and patient survival. 

Size: The gene expression data contains mRNA expression levels for 20531 genes across 585 patients and the number of patients with mRNA expression data are 300 patients 

Format:  

Gene Expression Data (data_mrna_seq_v2_rsem.txt): Rows represent 20,531 genes, and columns represent 300 patients with mRNA expression levels. 

Clinical Data (data_clinical_patient.txt & data_clinical_sample.txt): Contains 585 patients, with columns for clinical details like survival status, age, and tumour characteristics. 

Source: https://www.cbioportal.org/study/summary?id=ov_tcga_pan_can_atlas_2018 

Methodology:  

1. Data Processing & Exploration  

Acquire & load the data into R studio. 
Select relevant variables from the gene expression dataset, the sample dataset and the patient's dataset and clean the data to ensure consistency. 
Merge all three datasets to create a single, structured CSV file for analysis. 
Handle missing values, remove irrelevant or low-variance genes, and standardize numerical values. 
Test the distribution of gene expression values to determine if transformation is needed. 
Normalize the data if necessary. 
 
2. Dimensionality Reduction 

Apply PCA to reduce high-dimensional data. 
After PCA, the most informative features will be selected based on principal component loadings before classification. 
 

3. Supervised Classification Models  

Define survival groups using the median survival time to split patients into high-survival (greater than the median months) and low-survival (less than or equal to the median months). 
Split the data into training & test sets (80% train, 20% test). 
Train a Logistic Regression model and a Support Vector Machine (SVM) classifier to predict survival groups. 
Compare model performance using accuracy, precision, recall, F1-score. 

4. Conclusion and Interpretation 

Identify key genes associated with survival in OSC. 
Summarize findings and potential clinical implications. 
 
