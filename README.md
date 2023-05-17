# EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS

## INTRODUCTION
The files to be used for this task has the details on the names and locations of Bolton medical practices that have issued prescriptions for drugs to patients, drugs that can be prescribed, including the chemical substance and product description. The dataset could be used to examine trends and patterns in Bolton's medical practices’ prescription drug usage as well as the connections between the kinds of pharmaceuticals provided and the clinics that write them.

## DATA PREPARATION AND IMPLEMENTATION
For this task to be executed, the files drugs, medical practice and prescriptions containing the different prescriptions for patients are imported into the SQL server.
A database is therefore created for these files to be imported into.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/257e7ce7-3bbb-45e9-ae1e-ddc801697240)

## DRUG TABLE IMPLEMENTATION

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/fd920b2d-c1bd-4036-a168-04b336548e31)

DATA TYPE USED AND JUSTIFICATION
The data type that was used for the attributes in the drug entity was Nvarchar (50) and Nvarchar (100). This is because it is a variable width character string. It is used to define the string size in bytes and can be a value from 1 through 8,000 Unicode data.
Nvarchar (50) and Nvarchar (100) were used for the BNF_CODE, CHEMICAL_SUBSTANCE_BNF_DESCR, BNF_DESCRIPTION and BNF_CHAPTER_PLUS_CODE password because it is designed to cover all the characters of all languages. The drugs file for the prescriptions has been successfully updated into the SQL server.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/37906cee-4ba6-4327-af02-1d63e53120cf)


The BNF_CODE attribute was made the primary key for this table. This is because the BNF_CODE is a unique identifier for the columns in the drug table and this column does not have NULL values.
We can use the SELECT statement to view the values in the drug table.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/d4c730b0-1a29-4c78-8d98-e75b511fbc39)


## MEDICAL PRACTICE TABLE IMPLEMENTATION

The medical practice file was imported as a flat file into the SQL server.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/d6e3a4a8-9500-499d-abe4-34c36ed1c4f2)

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/2930430f-19f8-4756-bc33-387da3703039)


## DATA TYPE USED AND JUSTIFICATION

The data type that was used for the attributes in the drug entity was Nvarchar (50) This is because it is a variable width character string. It is used to define the string size in bytes and can be a value from 1 through 8,000 Unicode data.
Nvarchar (50) was used for practice_code, practice name, address_1, address_2, address_3, address_4 and postcode because it is a unicode datatype that is designed to cover all the characters of all languages. NULL values were allowed in address_2, address_3, address_4 because not all addresses have these details.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/524d6f29-153e-47e5-95f2-811a68432f17)

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/76115b5e-4b70-423e-a20e-bd2311b49333)


The practice code was added as the primary key for the table. This is because the values in the practice code column are unique and can be a unique identifier for the other columns in the table.
The SELECT statement was used to view the values contained in the medical practice file.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/8b173542-0890-40a6-869f-7561ba364cd5)


## PRESCRIPTIONS TABLE IMPLEMENTATION

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/cb1a5b75-c20b-45be-873a-3ada7ab83cb3)


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/13612901-7029-4a56-9fd2-f8d85da65b4c)

## DATA TYPE USED AND JUSTIFICATION

The int data type is the primary integer data type in SQL Server. It stores whole numbers that range from -2,147,483,647 to 2,147,483,647 for 9 or 10 digits of precision. The int data type was used for the prescription code and the items column because of the range of numbers in every prescription code and the number of items in each row in the item column.

The nvarchar(50) data type was used for the practice code and the bnf code column. This is because the nvarchar (50) is a unicode datatype that is designed to cover all the characters of all languages. 

The float data type was used as the data type for the quantity column to represent numbers more precisely than whole numbers. The float data type is used to store decimal or fractional numbers. The float data type was used in the quantity column because the column consists of both whole numbers and decimal numbers.
The money data type was used for the actual cost column. The money data type is used to record fixed-precision and fixed-scale monetary values. The money data type can store values up to 19 digits in length, with 4 of those digits to the right of the decimal point. This data type was used for the actual cost column because the money data type eliminates the possibility of rounding mistakes or data loss because of accuracy problems and ensures that calculations involving monetary values are correct and consistent.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/01a4b8f9-7cba-4889-a519-7ca49153f99f)


The prescription code column was used as the primary key because it has all unique values, and it can be used as a unique identifier for other columns on the prescription table.
The SELECT statement was used to view the values contained in the prescription table.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/2d7f10df-450b-4d76-9223-4f09b1d3482a)


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/6beb38f7-f5b3-4716-a54c-06b1bdc0ab34)


On the prescriptions table, two foreign keys were added to ensure that the medical practice table is properly linked to the prescription table and the drugs table is linked to the prescription table.
The foreign key constraint ensures that the values in the PRACTICE_CODE column in the prescriptions table match the values in the PRACTICE_CODE column in the medical practice table while the foreign key constraint ensures that the values in the BNF_CODE column in the prescriptions table match the values in the BNF_CODE column in the drugs table.
The foreign key constraints ensure referential integrity between the prescriptions and the medical practice table and the prescription and the drugs table.

## ENTITY RELATIONSHIP DIAGRAM BETWEEN THE TABLES

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/6f00c52a-b334-45ee-9d8b-b6c1f16bbd4b)


From this diagram we can infer that the prescriptions table is related to both the medical practice table and the drugs table. This is because the rows on the prescription table can be linked to the medical practice table using the practice code column. Also, because the prescription table can be linked to the drugs table using the BNF_CODE column.

## DETAILS OF DRUGS IN FORM OF TABLETS OR CAPSULES

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/e41de375-01b4-48a7-af2e-307e07e7c1fb)


SELECT statement was used to select FROM the drugs table. WHERE statement was used to retrieve information from the BNF_DESCRIPTION column on the drug table. The LIKE and OR function was used to retrieve words on like tablets or capsules present in the name of the drugs in every row in the BNF_DESCRIPTION column.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/68bf032c-6467-4bdd-8849-a581ccb5b567)


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/2436ba60-8d2a-4e98-9d55-2f75455adc85)


From the results derived, there are a total of 2,243 drugs that have words like tablets or capsules present in their names.

## TOTAL QUANTITY OF EACH PRESCRIPTIONS

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/4994c193-d9ff-424a-8cc3-e636693316a5)


SELECT statement was used to select the prescription code column FROM the prescriptions table.
The ROUND statement was used to round the numeric values to a specified number of decimal places. In this case, the round function was used to round the result derived from multiplying the ITEMS and QUANTITY columns to the nearest whole number.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/b6a9c80f-0306-4152-b923-134756738348)


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/59ae74a1-54e3-49f0-a15e-673d9c6cb8ec)


The derived result shows the total number of prescriptions by each prescription code.

## DISTINCT CHEMICAL SUBSTANCES ON THE DRUG TABLE

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/b8cc977f-a21e-414c-b944-c725913c8bbc)


The SELECT statement was used to select the CHEMICAL_SUBSTANCE_BNF_DESCR from the drugs table. The DISTINCT function was implemented to ensure that there are no duplicate values in the chemical substance result that would be derived. It ensures that only unique values are returned as the chemical substance on the drugs table.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/293deb65-141e-412e-b0f1-13d822ea5e89)


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/49fdc0aa-a2a6-44dd-a1f5-67636816a2ea)


With the derived result, the SELECT DISTINCT function filtered out the duplicate values in the chemical substance column on the drugs table. From the drugs table there was a total of 6,148 chemical substances. However, after implementing the select distinct function there is a total of 925 unique chemical substances on the drugs table.

## THE NUMBER OF PRESCRIPTIONS FOR EACH BNF_CHAPTER _PLUS_CODE SHOWING THE AVERAGE COST, MINIMUM AND MAXIMUM COST

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/b1d85478-b8fe-475b-84d9-511b9b344403)


The SELECT statement was used to select the BNF_CHAPTER_PLUS_CODE FROM the drugs table.
The COUNT function was used to count the number of prescriptions for each BNF chapter plus code.
The AVG function was used to count the average number of prescriptions for each BNF chapter plus code.
The MIN function was used to count the minimum number of prescriptions for each BNF chapter plus code.
The MAX function was used to count the maximum number of prescriptions for each BNF chapter plus code.
The INNER JOIN statement was used to join the drugs and the prescriptions table using the BNF_CODE column.
The GROUP BY statement was used to group the results by the BNF_CHAPTER_PLUS_CODE column of the drugs table. This means that the group by function will return one row for each unique value of the BNF chapter plus code column, and the aggregate functions (COUNT, AVG, MIN, MAX) will be applied to the values in the prescriptions table that matches each unique value of the BNF_CHAPTER_PLUS_CODE column.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/6de9da4c-50b4-460a-bcd5-d69011c58960)

From the result derived, Immunological Products and Vaccines BNF chapter plus code has the maximum cost of prescription of 21570.9208 while the average cost of this prescription is 1049.5574, Central Nervous System and Cardiovascular System BNF chapter plus code have the minimum cost of prescription of 0.1311 count while the average cost of these BNF chapter plus code are 28.3994 and 35.9956 respectively. The BNF chapter plus code with the highest count of prescription is Central Nervous System with a count of 28866.

## MOST EXPENSIVE PRESCRIPTION PRESCRIBED BY EACH PRACTICE

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/321f3b09-cb09-4d67-9cb9-f3195228d060)


The SELECT statement selects the practice name and bnf description column from the medical practice table. 
The INNER JOIN statement was used to combine the medical practice table, Prescriptions table, and drugs table based on the practice code and bnf code columns.
The GROUP BY statement was used to group the results by the practice name and bnf description columns.
The HAVING statement was used to filter the results to include only the rows where the maximum actual cost of prescription is greater than £4000.
The ORDER BY statement was used to sort the result of the maximum cost of prescription in descending order.


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/21f9e03e-385f-41a0-a60e-ff735725d2ab)


The result derived shows that there are a total of 15 medical practices that prescribe prescriptions not less than £ 4000. The Unsworth group practice prescribes Adjuvanted quadrivalent flu vacc (SA, inact) inj 0.5ml pfs at a maximum cost of 21570.9208 and this is the most expensive prescription by any medical practice.

## EXIST OR IN FUNCTION TO VIEW THE PRACTICE NAMES IN BOLTON, FARNWORTH, AND NAVIGATION PARK

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/900f8743-311e-494c-aee8-ded46a085401)


The SELECT FROM statement was used to select the columns from the medical practice table where the value in the address_3 column is equal to either 'Bolton', Farnworth, or navigation park'.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/36bab4d3-df64-4cdb-80bd-2785a4240f2b)

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/a75383ac-7de8-44f6-9b7c-fb3672a64310)


From the derived result, there is a total of 47 medical practices in bolton, farnworth and navigation park in the address_3 column on the medical practice table.

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/a68be1d2-18ea-4f0d-80f1-20c0a1ab62a0)


The SELECT statement was used to select the practice name from the medical practice table.
The WHERE EXISTS statement is a subquery that checks if there is a prescription code on the prescriptions table where the practice code matches the practice code in the medical practice table and the quantity is less than 100.
The second SELECT statement selects the prescription code column from the prescriptions table.
The WHERE statement joins the prescriptions table with the medical practice table on the practice code column.


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/7a2e1ecc-cdc4-45ae-884d-890a350599b0)


From the result derived, there are at least 60 practices that have issued less than 100 prescriptions to her patients.


## USING THE INNER JOIN FUNCTION

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/bf586366-fb86-4b8f-a4e3-75115adc6def)


The SELECT statement was used to select the prescription code and item columns from the prescriptions table, as well as the bnf description column from the drugs table.
The INNER JOIN statement was used to join the drugs table and the prescription table using the bnf code column.


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/e08d1b5a-e5c3-4faa-bde2-46330bd3ea55)


The derived result shows the number of items in each bnf prescription using their prescription code.

## USE OF SYSTEM FUNCTIONS

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/b3ba1c3c-0738-47dc-9392-5965dc42cf7c)


A function was created to help check the practice names of medical practices using their practice codes.

## USE THE GROUP BY, HAVING and ORDER BY FUNCTION

![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/94493ba7-97db-4883-973d-8d29099f451b)


The SELECT statement was used to select the practice name from the medical practice table.
The COUNT function was used to count the number of prescriptions for the medical practice that have the drugs paracetamol.
The JOIN statement joins the medical practice table and the prescription table using the practice code column. The prescription table was also joined with the drugs table using the bnf code column.
The WHERE function was used to filter rows where bnf description contains paracetamol.
The GROUP BY statement was used to the selected rows by the practice names.
The HAVING statement filters the group where the average actual cost is greater than 5.
The ORDER BY statement sorts the prescription count in descending order.


![image](https://github.com/Orlawlardey/EXAMINING-THE-TRENDS-AND-PATTERNS-IN-BOLTON-S-MEDICAL-PRACTICES-DRUG-PRESCRIPTIONS/assets/124607057/2fd43d19-d483-481a-9f69-f477adff8e8e)

The result derived shows that the Bolton community practice has a prescription count of 44 paracetamol drugs with the average cost of 41.1848.







