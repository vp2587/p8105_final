Proposal
================
Veerapetch Petchger, Clement Li, Heather Lu, Xiucheng (Eric) Zhang
2025-11-06

**1) The group members (names and UNIs)**

- Veerapetch Petchger: vp2587

- Clement Li: cl4773

- Heather Lu: hl3978

- Xiucheng (Eric) Zhang: xz3312

**2) The tentative project title**

Predicting Breast Cancer Outcomes from Clinical Features and Protein
Biomarkers

**3) The motivation for this project**

Breast cancer remains among the biggest threats to women’s health
worldwide. According to the WHO, it was the most common cancer in women
for 157 countries in 2022, leading to ~670000 deaths globally. However,
it is commonly known that early detection and treatment significantly
improves survival rates. This project aims to explore the relationships
among key clinical features in breast cancer cases, such as tumor size,
texture, and symmetry, to better understand the differences between
benign and malignant tumors. By visualizing and analyzing these
relationships, we hope to highlight meaningful patterns that can support
further research and awareness towards early detection.

**4) The intended final products**

The final product will be a comprehensive webpage featuring a navigation
bar with multiple sections: a homepage introducing the dataset, an
exploratory data analysis (EDA) section describing variable summaries
and data cleaning methods, and a statistical analysis section presenting
a multivariable logistic regression model of breast cancer outcomes,
anova comparison of biomarkers, and survival analysis. The webpage will
also include interactive visualizations and screencast recordings that
walk viewers through the dataset and each section of the site.

**5) The anticipated data sources**

This dataset is from Kaggle
(<https://www.kaggle.com/datasets/amandam1/breastcancerdataset/data>)
and contains a cohort of 334 breast cancer patients undergoing surgery
to remove their tumour. Variables include:

- Patient_ID: unique identifier id of a patient

- Age: age at diagnosis (Years)

- Gender: Male/Female

- Protein1, Protein2, Protein3, Protein4: expression levels (undefined
  units)

- Tumour_Stage: I, II, III

- Histology: Infiltrating Ductal Carcinoma, Infiltrating Lobular
  Carcinoma, Mucinous Carcinoma

- ER status (A protein that helps breast cancer cells grow in response
  to estrogen): Positive/Negative

- PR status (A protein that helps breast cancer cells grow in response
  to progesterone.): Positive/Negative

- HER2 status (A protein that helps breast cancer cells divide and
  spread.): Positive/Negative

- Surgery_type: Lumpectomy, Simple Mastectomy, Modified Radical
  Mastectomy, Other

- Date_of_Surgery: Date on which surgery was performed (in DD-MON-YY)

- Date_of_Last_Visit: Date of last visit (in DD-MON-YY) \[can be null,
  in case the patient didn’t visited again after the surgery\]

- Patient_Status: Alive/Dead \[can be null, in case the patient didn’t
  visited again after the surgery and there is no information available
  whether the patient is alive or dead\].

**6) The planned analyses / visualizations / coding challenges**

The first thing we will do is perfrom EDA on the BRCA.csv dataset. This
will include summaries of age, tumour stage, histology, hormone receptor
status (ER/PR/HER2), surgery type, and the four protein biomarkers. We
will examine distributions using histograms and boxplots, and create
stratified summaries (e.g., protein levels by tumour stage or histology)
to identify broad patterns that can guide subsequent modeling.

Our first main analysis will be multivariable logistic regression with
patient status (alive vs dead at last visit) as the outcome and
predictors will include age, tumor stage, surgery type, receptor status,
and selected protein markers from the EDA. We can then report the
adjusted odds ratio, and assess predictive performance through ROC
curves and AUC.

In addition to this, we also plan on conducting ANOVA comparisons on the
difference protein biomarkers across different groups, such as tumour
stage or histology type. his will allow us to test whether mean protein
expression differs systematically between groups. We will conduct
multiple-comparison tests after ANOVA results if necessary.

Third, we will perform basic survival analysis using the dates of
surgery, dates of last follow-up, and patient status. We will calculate
follow-up time for each patient and indicate whether they died during
follow-up or were still alive. Using this information, we will create
Kaplan–Meier survival curves to show how the probability of surviving
changes over time, both for the whole cohort and for subgroups such as
tumour stage or HER2 status.

In terms of visualizations, we plan to produce distribution plots and
boxplots for age and protein biomarkers, a correlation heat map of the
protein markers, Kaplan–Meier survival curves with risk tables, and
model-based plots such as ROC curves.

From a coding and workflow perspective, the project will involve
challenges involving date parsing, deriving follow-up time, factor
recoding, handling missing data, and working collaboratively in a shared
GitHub repository using a common RStudio project and regular
pull/commit/push cycles.

**7) The planned timeline**

November 6-7: Data collection, cleaning, and preliminary exploration.

November 10-14: Start multivariable logistic regression, ANOVA
comparison of biomarkers, and survival analysis.

November 15-25: Finalize all analyses and begin working on
visualizations.

November 26-30: Complete the draft report with visualizations and
interpretation.

December 1-6: Review and finalize the project for submission.

December 6-11: Prepare presentation for in-class discussion of projects.
