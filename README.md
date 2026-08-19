# Data-modeling-project-in-PowerBI
Building a data model that consist of a galaxy of star schema from twenty-three (23) chaotic and messy tables. 

## Table of Contents
- [Project Overview](#project-overview)
- [Tools & Technologies](#tools--technologies)
- [Dataset Explained](#dataset-explained)
- [Standards Applied](#standards-applied)
- [Dimension Tables](#dimension-tables)
- [Fact Tables](#fact-tables)
- [Building Relationships](#building-relationships)
- [Basic Measures and Visuals](#basic-measures-and-visuals)
- [Row Level Security](#row-level-security)

--------------------------------------------------------------------------------------------------------------
### Project Overview
This project builds from raw source data, a data model (the back bone)  for report analysis. A lot of cleaning and transformation was done in order to have proper tables. After that, related tables were merged in creating the dimension and facts tables, and relationships were established between them. This is a very key aspect, as all filters ride on the relationships.

![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Raw%20Model.png)

--------------------------------------------------------------------------------------------------------------

### Tools & Technologies
- Power BI
- Power Query
- DAX

--------------------------------------------------------------------------------------------------------------
### Dataset Explained
The source data was from an excel workbook which had 23 worksheets. Each worksheet was converted into a query/table. Data about entities such as product and customers were scattered across several worksheets and had to be merged.

![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Raw%20excel%20dataset2.png)

--------------------------------------------------------------------------------------------------------------
### Standards Applied
Uniformity and consistency is important in any project for all collaborators. Below are the Standards adhered to in this project:
+ Language - English
+ Naming conventions - Snake case
+ Table prefixes - "dim" (for dimension tables) and "fact" (for fact tables)
+ Identification of keys - _id (for source data) and _key (for Surrogate keys)


Likewise, data categorization and a uniform date format was applied ("yyyy-mm-dd") in the model


--------------------------------------------------------------------------------------------------------------
### Dimension Tables
Dimension tables are descriptive in nature. Related  tables with similar attributes were merged in creating each dimension table. The dim_clients table, dim_product table and dim_geo table, to mention a few, are the dimension tables created.

![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Grouping%20related%20tables.png)

--------------------------------------------------------------------------------------------------------------
### Fact Tables  
Fact tables are transactional. There are more than three fact table in this project, and in creating them, an eye had to be place on the grand total in order to forestall duplicating or truncating the figure.  

+ Below is the final constellation of star schema

![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Final%20model.png)

--------------------------------------------------------------------------------------------------------------
### Building Relationships  
The project was based on a star schema and several one to many (1-*) relationships were established between dimension and fact tables. However, in creating the row-level security, a one to one relationship had to be established between the security tables and the dim_client table.  The dim_geo table served as a role-playing dimension table to the fact_sales table, with one the relationship being inactive.  

+ Below is the Manage Relationship dialogue box showing the several relationships created

![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Manage%20relationship.png)  

+ Below is the dim_geo table serving as a role playing dimension table
  
![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Role%20playing%20dimension.png)


--------------------------------------------------------------------------------------------------------------
### Basic Measures and Visuals  
Building reports was not the primary aim of the project, therefore, only basic table and card visuals were created for demonstration purposes. ALL measures created were inserted into a table called "_measures" which can be seen at the top of the data pane in report view.  

+ Below is the depiction of the visual created

![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Basic%20visual%20.png)

--------------------------------------------------------------------------------------------------------------
### Row Level Security  
Stakeholders wanted two (2) row-level securities for: 
+ Client managers
+ Regional managers

Once the relationships were established between the security tables and the dim_client table, the two roles were created and DAX was used in retuning the values relevant to each users. The roles were tested to confirm operability.  

+ Showing below are the DAX for the two (2) row-level securities

![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Dax%20code2.png)
![Alt text](https://github.com/Oyetola-Project-Profile/Data-modeling-project-in-PowerBI/blob/main/images/Dax%20code3.png)


--------------------------------------------------------------------------------------------------------------









<details>
<summary>Click to expand</summary>
More hidden content here...
</details>
