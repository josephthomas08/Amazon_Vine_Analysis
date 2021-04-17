# Amazon_Vine_Analysis
Sellby Amazon reviews 





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



#### D1.2.2 products Table loaded in PG-Admin 


<img width="370" alt="D1 2 3 products table " src="https://user-images.githubusercontent.com/75267605/115099897-f8ef8900-9f06-11eb-8e3c-9557a2043260.png">




#### D1.2.3 Review Id Table loaded in PG-Admin 


<img width="625" alt="D1 2 4 review id table " src="https://user-images.githubusercontent.com/75267605/115099901-03aa1e00-9f07-11eb-9742-a31d931dd284.png">




## Deliverable 2: Determine Bias of Vine Reviews


### There is a DataFrame or table for the vine_table data using one of three methods above - Used pyspark 


<img width="1564" alt="D2 1 0" src="https://user-images.githubusercontent.com/75267605/115119459-6b4b8200-9f76-11eb-8f3f-b85330532ec2.png">



### Recreate the VIne Table and data is filtered to create a DataFrame  where there are 20 or more total votes

<img width="945" alt="D2 1 1" src="https://user-images.githubusercontent.com/75267605/115119498-a8177900-9f76-11eb-8198-4f1b5a7fe96c.png">

<img width="1319" alt="D2 1 2" src="https://user-images.githubusercontent.com/75267605/115119500-ac439680-9f76-11eb-8a44-02dc6b60c159.png">




### The data is filtered to create a DataFrame or table where the percentage of helpful_votes is equal to or greater than 50% 

<img width="1536" alt="D2 1 3" src="https://user-images.githubusercontent.com/75267605/115119512-b4033b00-9f76-11eb-9bce-aa63386e8408.png">

### The data is filtered to create a DataFrame or table where there is a Vine review 

<img width="999" alt="D2 1 4" src="https://user-images.githubusercontent.com/75267605/115119521-be253980-9f76-11eb-9b47-f67975279381.png">

### The data is filtered to create a DataFrame or table where there isn’t a Vine review 

<img width="1010" alt="D2 1 5" src="https://user-images.githubusercontent.com/75267605/115119527-c54c4780-9f76-11eb-907c-79257694c82c.png">


### The total number of reviews, the number of 5-star reviews, and the percentage 5-star reviews are calculated for all Vine and non-Vine reviews 

<img width="585" alt="D2 1 6-7" src="https://user-images.githubusercontent.com/75267605/115119529-c8473800-9f76-11eb-9570-c13bbaf9c5d5.png">


<img width="570" alt="D2 1 8-9" src="https://user-images.githubusercontent.com/75267605/115119530-cd0bec00-9f76-11eb-8a87-128b1ea60629.png">


<img width="812" alt="D2 1 10-11" src="https://user-images.githubusercontent.com/75267605/115119538-dc8b3500-9f76-11eb-851c-9af7aae3d3b2.png">


### Additional Analysis 


<img width="596" alt="D2 2 1-2" src="https://user-images.githubusercontent.com/75267605/115119545-e6149d00-9f76-11eb-9bcd-9aab08e31a07.png">


<img width="768" alt="D2 2 3-4" src="https://user-images.githubusercontent.com/75267605/115119546-e90f8d80-9f76-11eb-98de-8c65db4d809e.png">


## Deliverable 3: A Written Report on the Analysis 



