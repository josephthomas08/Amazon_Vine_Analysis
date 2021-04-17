# Amazon_Vine_Analysis
## Sellby Amazon reviews 


### 1. Overview

The project is to expose the Amazon Vine program devloped by Amazon to understand, document, expand and analyse the product rating based on paid and unpaid reviews from the ever expanding cilientiele. The companies , service and manufacturing companies pay a small fee towards this program where in products are offered to Vine members who are then required to publish a review for the products and services. I have utlized the pySPark tool to extract, transform and load the home improvement dataset from Amazon reviews using Google COlab.


### Resources
#### 1. Data Source: Amazon Review datasets, Home improvement 
#### 2. Software: Google Colab Notebook, PostgreSQL 13.2, pgAdmin 4, AWS


## Deliverable 1: Perform ETL on Amazon Product Reviews

### D1.0 An Amazon Review dataset is extracted as a DataFrame 



<img width="1605" alt="D1 1 0 extracted_dataframe" src="https://user-images.githubusercontent.com/75267605/115099762-09ebca80-9f06-11eb-9fb7-c00752b87b88.png">




### D1.1 The extracted dataset is transformed into four DataFrames with the correct columns 

#### D1.1.1 - Vine Table


<img width="1063" alt="D1 1 1 vine_table" src="https://user-images.githubusercontent.com/75267605/115099767-1112d880-9f06-11eb-9e3f-c0c0cfe69930.png">


#### D1.1.2 - Customers Table

<img width="1175" alt="D1 1 2 customers_table" src="https://user-images.githubusercontent.com/75267605/115099772-1708b980-9f06-11eb-85b7-e02f4ea33cf5.png">


#### D1.1.3 - Products Table

<img width="837" alt="D1 1 3 products_table" src="https://user-images.githubusercontent.com/75267605/115099776-1b34d700-9f06-11eb-97c9-bb81a8d1113c.png">



#### D1.1.4 - review id Table

<img width="1308" alt="D1 1 4 review_id_table" src="https://user-images.githubusercontent.com/75267605/115099781-1f60f480-9f06-11eb-8620-c271e9ba79b2.png">


### D1.2 four DataFrames are loaded into their respective tables in pgAdmin 

#### D1.2.1 Vine Table loaded in PG-Admin 


<img width="700" alt="D1 2 1 Vine table" src="https://user-images.githubusercontent.com/75267605/115099886-e5dcb900-9f06-11eb-856a-3f9bb7e7637e.png">


#### D1.2.2 Customers Table loaded in PG-Admin 


<img width="351" alt="D1 2 2 Customers Table " src="https://user-images.githubusercontent.com/75267605/115099891-eaa16d00-9f06-11eb-9089-56249712d0b9.png">



#### D1.2.3 products Table loaded in PG-Admin 


<img width="370" alt="D1 2 3 products table " src="https://user-images.githubusercontent.com/75267605/115099897-f8ef8900-9f06-11eb-8e3c-9557a2043260.png">




#### D1.2.4 Review Id Table loaded in PG-Admin 


<img width="625" alt="D1 2 4 review id table " src="https://user-images.githubusercontent.com/75267605/115099901-03aa1e00-9f07-11eb-9742-a31d931dd284.png">




## Deliverable 2: Determine Bias of Vine Reviews


### DataFrame for the vine_table data using one of three methods above - I have used pyspark 


<img width="1564" alt="D2 1 0" src="https://user-images.githubusercontent.com/75267605/115119459-6b4b8200-9f76-11eb-8f3f-b85330532ec2.png">



### Recreated the Vine Table and data is filtered to create a DataFrame  where there are 20 or more total votes

<img width="945" alt="D2 1 1" src="https://user-images.githubusercontent.com/75267605/115119498-a8177900-9f76-11eb-8198-4f1b5a7fe96c.png">

<img width="1319" alt="D2 1 2" src="https://user-images.githubusercontent.com/75267605/115119500-ac439680-9f76-11eb-8a44-02dc6b60c159.png">




### The data is filtered to create a DataFrame where the percentage of helpful_votes is equal to or greater than 50% 

<img width="1536" alt="D2 1 3" src="https://user-images.githubusercontent.com/75267605/115119512-b4033b00-9f76-11eb-9bce-aa63386e8408.png">

### The data is filtered to create a DataFrame where there is a Vine review 

<img width="999" alt="D2 1 4" src="https://user-images.githubusercontent.com/75267605/115119521-be253980-9f76-11eb-9b47-f67975279381.png">

### The data is filtered to create a DataFrame where there isn’t a Vine review 

<img width="1010" alt="D2 1 5" src="https://user-images.githubusercontent.com/75267605/115119527-c54c4780-9f76-11eb-907c-79257694c82c.png">


### The total number of reviews, the number of 5-star reviews, and the percentage 5-star reviews are calculated for all Vine and non-Vine reviews 

<img width="585" alt="D2 1 6-7" src="https://user-images.githubusercontent.com/75267605/115119529-c8473800-9f76-11eb-9570-c13bbaf9c5d5.png">


<img width="570" alt="D2 1 8-9" src="https://user-images.githubusercontent.com/75267605/115119530-cd0bec00-9f76-11eb-8a87-128b1ea60629.png">


<img width="812" alt="D2 1 10-11" src="https://user-images.githubusercontent.com/75267605/115119538-dc8b3500-9f76-11eb-851c-9af7aae3d3b2.png">



The big idea of this big Data study is to understand if their is any bias toward favorable reviews from vine members.


### 2. Results

#### 2.1 Number of vine and nonvine members


<img width="585" alt="D2 1 6-7" src="https://user-images.githubusercontent.com/75267605/115119529-c8473800-9f76-11eb-9570-c13bbaf9c5d5.png">


From the above analysis we see the following 

##### Paid review is 266
##### unpdaid review is 38829





#### 2.2 Number of 5 star vine and non vine reviewers.



<img width="570" alt="D2 1 8-9" src="https://user-images.githubusercontent.com/75267605/115119530-cd0bec00-9f76-11eb-8a87-128b1ea60629.png">



From the above analysis we see the following 

##### Paid Vine 5 Star reviews are 125
##### Unpaid or non- vine reviews are 18246


#### 2.3 Percentage of five start vine and non vine reviews 

<img width="812" alt="D2 1 10-11" src="https://user-images.githubusercontent.com/75267605/115119538-dc8b3500-9f76-11eb-851c-9af7aae3d3b2.png">


From the above analysis we see the following 

##### Paid Vine % 5 Star reviews is 47 % 
##### Unpaid or non- vine  % 5 star reviews is 47 % 

The percentage for 5 star analysis reveals the chances of bias bewteen vine and non-vine members or paid and unpaid members is not very much visible.





### 3 Summary: 
The analysis overall in the 5 star review did not provide us with any noticable difference between paid and unpaid reviews but additional analysis with 4 star added on to the analysis will provide us with better understanding of the bias difference between paid and unpaid reviews.


 To further evaluate the study additional analysis to incorporate the 4 star along with 5 star  review is conducted which is as displayed below.
### Additional Analysis 


<img width="596" alt="D2 2 1-2" src="https://user-images.githubusercontent.com/75267605/115119545-e6149d00-9f76-11eb-9bcd-9aab08e31a07.png">


<img width="768" alt="D2 2 3-4" src="https://user-images.githubusercontent.com/75267605/115119546-e90f8d80-9f76-11eb-98de-8c65db4d809e.png">



##### Paid Vine % 5 Star reviews is 76 % 
##### Unpaid or non- vine  % 5 star reviews is 63 % 

In this analysis we see a susbtantial difference of 13 % in paid and unpaid review. We can fairly say now that the paid Vine members does create substantial bias. This bias will be more evidennt when we include 3 star review along with 4 and 5 star by  paid Vine members to improve the visibility and credibility of manufacturers, companies, suppliers and service providers.






