# Cloud-Computing-Pratham
Overview of Projects on Amazon Web Services (AWS)
## Data Wrangling Project

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



## Exploratory Data Analysis

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
- Exoloring the Data and filtering to only see the rows with adult students (Age > 18)
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


  


