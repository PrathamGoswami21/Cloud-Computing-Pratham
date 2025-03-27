# Cloud-Computing-Pratham

Overview of Projects on Amazon Web Services (AWS)



## Data Wrangling Project - UCW PLAR Procedure


**Project Description**: Data Wrangling of Document List, Portfolio List and Student List Datasets of UCW's PLAR Procedure

**Project Title**: Data Wrangling for enhanced PLAR Data Analytics

**Objective**: The primary goal of this project is to perform comprehensive data wrangling to prepare datasets for data analytics of the PLAR procedure by profiling, cleaning, transforming, and cataloging the datasets to help in better data analytics of UCW's PLAR procedure.

**Background**: University Canda West has accumulated data for their PLAR procedure in the form of multiple datasets including Document lists, Portfolio Lists and Student Lists. However, this data can be inconsistent, incomplete, or fragmented, making it challenging to derive meaningful insights. Effective data wrangling will facilitate better decision-making.

**Datasets**: The data wrangling process will involve three datasets, including:
- Student List: Student records that include student IDs, Names, Age, Gender, Grade, Major, Email, Phone Number and GPA
- Document List: Document details such as document ID, Title, Author, File Type, Access Level, Category, Size, Owner
- Portfolio List: Portfolio detils including, ID, names, owner, category, Number of projects, Primary Skill, Rating Visibility.

**Design for The AWS Cloud Platfrom for Data Wrangling**

![Screenshot 2025-03-26 165701](https://github.com/user-attachments/assets/84fea2be-8200-43c6-a0a1-896243166eeb)


**Methodology/Steps** 

**Data Profiling** - Profiling the datasets using AWS GlueDataBrew.
- Student List Profiling
  
![Screenshot 2025-03-26 155147](https://github.com/user-attachments/assets/2e0ca53b-12c0-42ef-a25f-f9f211f565cb)

- Document List Profiling
  
  ![Screenshot 2025-03-26 155538](https://github.com/user-attachments/assets/1a8199af-d6d9-411c-8dd8-2a0522e251f3)
  
- Portfolio List profiling
  
  ![Screenshot 2025-03-26 155551](https://github.com/user-attachments/assets/85506179-f372-465c-b2f2-11ebb77b1c7f)
  
**Data Cleaning** - Cleaning the three datasets using AWS GlueDataBrew Projects to remove outliers, address missing values and correcting other inconsistencies

- Student List cleaning
  
  ![Screenshot 2025-03-26 160107](https://github.com/user-attachments/assets/880a5181-1406-48f2-b96e-29dd5e68cdf8)
  
- Document List cleaning
  
  ![Screenshot 2025-03-26 160126](https://github.com/user-attachments/assets/3d758a9a-0189-4070-b115-b2cd191affcd)
  
- Potfolio List Cleaning
  
  ![Screenshot 2025-03-26 160458](https://github.com/user-attachments/assets/41389097-dffc-482b-8c15-5c0ca3c4c9a0)

**Data Cataloging** - Using Crawlers in AWS Glue to create a database containing tables for each of the three datasets.

  ![Screenshot 2025-03-26 161637](https://github.com/user-attachments/assets/d3e72582-a004-4c98-bb1d-ec28079c45a7) *Data crawler*

  ![Screenshot 2025-03-26 161622](https://github.com/user-attachments/assets/ee346993-8c32-4ec0-9bf5-bb88f24d8456) *Database Catalog With Tables*

  
**Tools and Technologies:**
- AWS GlueDataBrew for data profiling and cleaning.
- AWS Glue for data cataloging using Crawlers.

**Deliverables:**
- A profiled, cleaned and cataloged group of datasets ready for analysis and available in a suitable format such as CSV or Parquet
- A report documenting the data wrangling process, including challenges encountered, methods employed, and final dataset characteristics.



## Exploratory Data Analysis - Student Data from UCW's PLAR Procedure

**Project Description**: Studying, exploring and performing initial analysis of Student List dataset of UCW's PLAR procedure.

**Project Title**: Exploring the Student List Dataset of UCW's PLAR Procedure

**Objective**: The primary goal of this project is to explore the various characterstics of the student list dataset of UCW's PLAR procedure, including its schema, column, content and basic summarization. 

**Background**: University Canda West has accumulated student data for their PLAR procedure in the form of Student Lists dataset. The university now wants to perform meaninful analysis on this data in order to improve their PLAR services. 

**Datasets**
- Student List: Student records that include student IDs, Names, Age, Gender, Grade, Major, Email, Phone Number and GPA



### Draw.Io Design Diagram for EDA on AWS

- ![Screenshot 2025-03-26 171812](https://github.com/user-attachments/assets/28c1527f-6ec4-4d72-8ddd-09a3dfc1745b)



**Methodology/Steps**

**Data Collection and Preparation**:
- Creating a new AWS Glue Visual ETL Job
- Loading the Student List data from the relevant AWS Glue data catalog tables
- Perform initial data cleaning and organisation steps which includes renaming columns for clarity and dropping irrelevant columns such as email and phone number.
![Screenshot 2025-03-26 170934](https://github.com/user-attachments/assets/536cc1a6-678f-4dd1-80bf-75a97f669111)


**Data Exploration and Filteration**
- Expoloring the Data and filtering to only see the rows with adult students (Age > 18)
  ![Screenshot 2025-03-26 171009](https://github.com/user-attachments/assets/c1e9cea9-154d-4d1b-b42f-580fe4c0e8cf)

  
**Initial Exploratory Data Summarization**
- Aggregating data using AWS Glue's Aggregate Node with grouping by column 'major' with 'age' column to be aggregated by the fucntion 'average'.
- Adding summarzing date in local time zone.
  ![Screenshot 2025-03-26 171112](https://github.com/user-attachments/assets/7ee47eb3-eeb5-4a32-b556-8bdeb9b321ee)

**Storing Data**
- Loading summarized data and its reports in the curated Amazon S3 bucket.



 ***Complete Visual ETL for Student List data exploration and Summarization***


![Screenshot 2025-03-26 171954](https://github.com/user-attachments/assets/5c665d56-e28e-480b-ab0f-236783c752cc)


  
**Tools and Technologies**
- AWS Glue

**Deliverables**
- A comprehensive Visual ETL containing all steps of extraction, cleaning, filtering and summarizing.
- A detailed exploration of the dataset in question.


  

## Descriptive Analysis - City of Vancouver

**Project Description**: Descriptive Analysis of City of Vancouver's 311-contact center data using the city's AWS DAP. 

**Project Title**: Understanding and Answering Business Questions for City of Vancouver's 311-contact center data using the city's AWS DAP. 

**Objective**: The primary goal of this project is to conduct a descriptive analysis of City of Vancouver's 311-contact center data using the city's AWS cloud DAP.  Through this analysis, we aim to summarize key characteristics of the dataset and to answer the following business questions: 1. What was the average service level per month for the 311-contact center in the year 2024? 2.	What was the maximum numbers of calls City of Vancouver’s contact center handled per month in 2024?

**Background**: City of Vancouver has migrated to AWS for its cloud computing needs and wants to have a cloud based Data Analytic Platform (DAP) to answer some important business questions for its 311-contact-center. 


**Dataset**: The dataset contains city of vancouver's 311 contact center data from the year 2024 with the columns; Date, Calls Offered, Calls Handled, Calls Abandoned, Service Level, Average time of answering and BI_ID. 



***Draw.io Diagram for the Implementation of the City's DAP on AWS***

![image](https://github.com/user-attachments/assets/63e89daa-3e36-4d82-9afa-78d7ce086588)


**Methodology/Steps**

**Data Collection** - The data was collected and sourced from City of Vancouver's data portal and then uploaded in the raw Amazon S3 bucket. 

![Screenshot 2025-03-26 182253](https://github.com/user-attachments/assets/10fb60b7-b82e-42c9-9a5a-d85f398f6fda)


**Data Preparation**
- AWS GlueDataBrew was used to profile the dataset in order to better understand its schema, correlations and overall characterstics.

![Screenshot 2025-03-26 182455](https://github.com/user-attachments/assets/eed2bc1d-3015-4942-864b-f5e5624c754e) *311-Contact center data profile*


- By creating a project on DataBrew, the dataset was cleaned by renaming columns, formatting date and by addressing other issues.

  ![Screenshot 2025-03-26 182725](https://github.com/user-attachments/assets/b45405ff-8802-4e71-ae3c-abcd5c075835) *Recipe depicting data cleaning steps*


**Data Cataloging** - AWS Glue was used to create a database catalog for the dataset and Glue's Crawlers were used to create tables from the dataset. 

  ![Screenshot 2025-03-26 183753](https://github.com/user-attachments/assets/e66b4a18-ad66-4ba8-b295-5929833508aa) *Data Catalog & Tables*


**Initial Data Exploration** 

  - Using AWS Glue's Visual ETL, the dataset was explored and further prepared for the descriptive analysis by taking important steps such as changing schema, and filtering the dataset to only inlcude days where more than 200 calls were offered by the contact center. Some initial summarization in the form of overall average service level were also performed to better know the dataset.


    ![Screenshot 2025-03-26 184822](https://github.com/user-attachments/assets/3cd662c9-1a94-4d08-aed2-d66343af0b53) *Complete Visual ETL for Data exploration*



**Descriptive Statistics**

  - based on the filtered and cleaned data, AWS Athena was used to run SQL queries on the dataset to produce the required descriptive statistics. 

    ![Screenshot 2025-03-26 185150](https://github.com/user-attachments/assets/589f09d9-d5c7-4de2-b965-58fc227c94d8) *Consolidated SQL Query*   


    ![Screenshot 2025-03-26 185413](https://github.com/user-attachments/assets/4ed4777a-05de-40ac-b9a4-0d5600c7286f)  *Output of the SQL Query*



    ![Screenshot 2025-03-26 185744](https://github.com/user-attachments/assets/0f05eaf5-9a12-4561-8097-c4782a41070b) *Storage location of summarized statistics* 




**Tools and Technologies**
- AWS S3 for data storage
- AWS GlueDataBrew for data profiling and Cleaning
- AWS Glue for data cataloging, crawling and Visual ETLs
- AWS Athena for descriptive statistics through SQL queries. 


**Deliverables**
- Answers to the business question in the form of the SQL query results that are stored in the curated S3 bucket of city of Vancouver's contact center data DAP. 






## Data Quality Control - UCW PLAR Procedure


**Project Description**: Implementation of Data Quality Control For the Document Data of UCW's PLAR Procedure

**Project Title**: Data Quality Control Steps for UCW's PLAR procedure. 

**Objective**: The primary objective of this project is to perform a data quality control check on the dataset related to the documents submitted during UCW's PLAR process. These steps will ensure the accuracy, completeness, consistency, and freshness of the data. 

**Background**: University Canada West has seen an increase in the number of potential students seeking recognition of their prior learning. To make sure the decision making is accurate the university wants to have a detailed quality control check for its 'Document List" dataset of its PLAR procedure. 



***Draw.io design for the quality check implementation in AWS Console***
![Screenshot 2025-03-26 194428](https://github.com/user-attachments/assets/61515ec4-9429-4da5-a922-9e8da17bfd8b) 

**Methodology/Steps** 

**Data Extraction**: The document data for quality check was extracted from the raw Amazon S3 bucket into a AWS Glue Visual ETL Job

**Data Quality Evaluation** : AWS Glue's data evaluation node was used for this step to check the freshness, uniqueness and completeness of the dataset through the following rules on relevant schemas
   - *Rules = [ Completeness "author" >= 0.95, 
Uniqueness "document id" > 0.99,
DataFreshness "date created" < 600 days]*

**Data Conditional Routing** : After the implementation of data quality rules, the dataset was divided among the rows that passed the test and those that did not through the conditional router node of AWS Glue. 

**Data Load Preparation**: The data was then adjusted by changing schema, dropping newly created unncesaary columns and by instructing AWS Glue to only have one partition. 

**Data Loading**: The data that passed and failed the quality control rules was then loaded in the transformed data S3 bucket in the 'passed' and 'failed' and subfolders of the quality control folder of document list dataset, respectively. 





***Complete AWS Glue Visual ETL for Data Quality Control***
![Screenshot 2025-03-26 200436](https://github.com/user-attachments/assets/388375b3-2769-4193-8763-eace14f5b0dc)



***Failed Data Loaded in the relevant subfolder***
![Screenshot 2025-03-26 200507](https://github.com/user-attachments/assets/f3bf7a7e-5aec-4bac-b126-46855957d220)



***Quality passed data loaded in the 'Passed' subfolder***
![Screenshot 2025-03-26 200534](https://github.com/user-attachments/assets/56f6d0b7-6434-4ebd-92b1-dffd342a9f5b)


**Tools and Technologies**
- AWS Glue
- AWS S3



Deliverables:
- Document list dataset consisting of rows that passed the quality control.
- Identification of rows that did not pass the quality check.
- Separate storage for quality check passed and failed data points of document list dataset for better analysis and evaluation.







## AWS Cloud Foundation Badge 

Link : https://www.credly.com/badges/0020c46e-eb09-4cb7-b284-bd916a1c2ab6/public_url

Badge:

<div data-iframe-width="150" data-iframe-height="270" data-share-badge-id="0020c46e-eb09-4cb7-b284-bd916a1c2ab6" data-share-badge-host="https://www.credly.com"></div><script type="text/javascript" async src="//cdn.credly.com/assets/utilities/embed.js"></script> 

![aws-academy-graduate-aws-academy-cloud-foundations](https://github.com/user-attachments/assets/2d2fa354-e798-4c56-8070-0e64de149e3d)

