Introduction to COS-analysis package
====================================

**COS-analysis** is a Python package developed to standardize the data loading and preprocessing. It aims to enhance data quality, reduce inconsistencies, and streamline the process of data preparation for analysis.

Get started
-----------

The COS Analysis Package is built on the dmpy API, which has been developed by Imperial College London to facilitate access to data. 

**Installation and usage:**

The COS Analysis Package is pre-installed on the Analytical Environment. The primary objective is to run analyses directly within this environment, ensuring seamless integration with existing data sources and computational resources.

Main functionalities
--------------------

This package provides functionality to:

* Read, concatenate, clean, and save device datasets on the DMP.

* Read and clean diary data by choosing a specific concept of interest (e.g.,fatigue, daytime sleepiness, or sleep quality), applying a defined window size, and deciding whether to consider changes from baseline.

* Combine and aggregate device and diary datasets, incorporating the covariates specified in the SAP, with the option to filter by cohort.

* Preprocess the dataset to prepare it for analysis.

* Upload a model to the DMP.

* Run inferences on pre-saved models.

Available Data Types
--------------------

**Feature data**

* "SLP_night" - Sleep features over the night (derived from BED sensor)
* "HRV" - Heart Rate Variability - 5minutes (derived from VTP)
* "VIT" - Vital Signs - 1minute (derived from VTP)
* ("GVA" - Gait Variability - 24h / daily)
* "MCR_MCR" - Activity features 1 - 1minute (derived from AX6)
* "MCR_MCL" - Activity features 2 - 1minute (derived from AX6)
* "STS" - Sit To Stand transitions - Events (derived from AX6)
* "COG_pvt" - Cognitive test 1 every morning (derived from CANTAB App)
* "COG_dst" - Cognitive test 2 every evening (derived from CANTAB App)

[See full list of features in D7.3](https://newcastle.sharepoint.com/:b:/r/sites/idea-fast/Shared%20Documents/Work%20Packages/WP7%20Statistical%20Inference,%20Design%20and%20Learning/Deliverables/D7.3/IDEA-FAST_D7.3_AI-Methods-Toolbox_v1.0-merged.pdf?csf=1&web=1&e=aJwdfM)

[See dataset format](https://newcastle.sharepoint.com/:x:/r/sites/idea-fast/_layouts/15/Doc.aspx?sourcedoc=%7B0D52C3F4-CE5B-4FDC-8EAB-2FF2FFB9BF2E%7D&file=COS_Standardized_Feature_Data_Format.xlsx&action=default&mobileredirect=true)

**ADAM dataset data**

* Demographics from ADSL: COHORT, AGE, GENDER, BMI, TIMESINCEDIAG.
* PROs from ADPRO : FACITF-SCORE, SLPD4, KSS, fVAS, sqVAS.
* Baseline of PROs from ADPRO (value at the start of the first TUP): FACITF-SCORE_baseline_7days, KSS_baseline_7days, SLPD4_baseline_7days.
* Clinical data from ADCL: Disease score.
* Diaries from ADDI: Answers to questionnaires recorded three times a day - overall_fatigue_vas, physical_fatigue_vas, mental_fatigue_vas, sleep_quality_vas, KSS.