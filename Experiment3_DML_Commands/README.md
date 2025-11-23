# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
<img width="945" height="198" alt="image" src="https://github.com/user-attachments/assets/5e75f954-5fcc-4b1e-9384-3db5f808d753" />


```
update products
set product_name= 'Grapefruit'
where product_id=4;
```

**Output:**

<img width="1196" height="174" alt="image" src="https://github.com/user-attachments/assets/993cafa8-53fa-401b-8d9a-b89a82de3ed8" />


**Question 2**
---
<img width="1034" height="588" alt="image" src="https://github.com/user-attachments/assets/9afdf45a-8d0e-4fe7-81f7-74f73024f4c3" />

```sql
update Employees 
set hire_date='2024-01-24'
where department_id=50;
```

**Output:**

<img width="1208" height="238" alt="image" src="https://github.com/user-attachments/assets/bd1dc2a1-8481-43a4-862f-00007b602e8f" />


**Question 3**
---
<img width="1238" height="538" alt="image" src="https://github.com/user-attachments/assets/e039e0a8-88d6-4e3b-8eca-f4f69bdfb018" />


```
update PRODUCTS 
set reorder_lvl=reorder_lvl*0.7
where product_name like '%cream%'
and quantity>reorder_lvl;
```

**Output:**

<img width="733" height="443" alt="image" src="https://github.com/user-attachments/assets/18199352-e7ee-43aa-8bcd-a48a2ceee12a" />
<img width="810" height="436" alt="image" src="https://github.com/user-attachments/assets/3d531a05-8e99-44c4-a8ab-4ca9a96db71a" />
<img width="875" height="428" alt="image" src="https://github.com/user-attachments/assets/924d16ec-b048-4d57-8788-3480443a08d7" />


**Question 4**
---
<img width="1259" height="479" alt="image" src="https://github.com/user-attachments/assets/9e27b26b-3759-4fdf-8fb7-d4c7143ef7af" />


```
update products
set reorder_lvl=reorder_lvl*1.3
where category='Food'
and quantity<reorder_lvl*0.5;
```

**Output:**

<img width="1223" height="361" alt="image" src="https://github.com/user-attachments/assets/c618f62a-de2e-48d9-a622-1c568d37ee10" />
<img width="867" height="337" alt="image" src="https://github.com/user-attachments/assets/e0b1404b-1ea5-43fd-9650-827d36e67da6" />


**Question 5**
---
<img width="707" height="98" alt="image" src="https://github.com/user-attachments/assets/63ad3efd-126a-45fe-ac42-12fb73217798" />


```
update Customer
set grade=5
where city='Chennai';
```

**Output:**

<img width="948" height="408" alt="image" src="https://github.com/user-attachments/assets/349f8170-41fc-4e84-9d86-915bb1873592" />
<img width="583" height="412" alt="image" src="https://github.com/user-attachments/assets/ab144dd0-0edc-43dd-b477-c6a76554a610" />


**Question 6**
---
<img width="1266" height="635" alt="image" src="https://github.com/user-attachments/assets/10f02fe9-20b5-477d-97ae-3c13dab096c8" />


```
delete from Customer
where grade<2;
```

**Output:**

<img width="743" height="487" alt="image" src="https://github.com/user-attachments/assets/ec206c48-ec06-4230-99fb-342b0259038a" />


**Question 7**
---
<img width="1244" height="607" alt="image" src="https://github.com/user-attachments/assets/53620061-e99d-486a-a70d-d0f53c032d81" />


```
delete from Customer
where GRADE>=2;
```

**Output:**

<img width="849" height="488" alt="image" src="https://github.com/user-attachments/assets/2d0952ab-31bf-4dab-afe1-4c1d0aa05c62" />


**Question 8**
---
<img width="1261" height="690" alt="image" src="https://github.com/user-attachments/assets/6b0a4397-ce4b-4e89-bcaf-ac4dd4e8c086" />



```
delete from Customer
where OPENING_AMT between 4000 and 6000;
```

**Output:**

<img width="1230" height="536" alt="image" src="https://github.com/user-attachments/assets/b51bfa73-705c-4630-acc9-3e1d88e293aa" />
<img width="442" height="519" alt="image" src="https://github.com/user-attachments/assets/7dd5308c-b659-4aa2-947f-44f3850afdb6" />

<img width="1223" height="542" alt="image" src="https://github.com/user-attachments/assets/3e933ffb-8fd0-4ac8-8d03-b4889de347d9" />


<img width="732" height="510" alt="image" src="https://github.com/user-attachments/assets/0584b481-3b13-40f9-9a30-09e93a82a900" />


**Question 9**
---
<img width="1241" height="438" alt="image" src="https://github.com/user-attachments/assets/a38409a8-5f12-407f-97f8-ac139b08a846" />


```
delete from Customer
where CUST_COUNTRY='UK'
and WORKING_AREA='London'
and GRADE <3;
```

**Output:**

<img width="1127" height="400" alt="image" src="https://github.com/user-attachments/assets/eff81355-25c6-4921-9597-8dd3b78fba51" />
<img width="1165" height="401" alt="image" src="https://github.com/user-attachments/assets/c52d56b7-6dbf-469a-be68-8021b8fc38f2" />
<img width="753" height="376" alt="image" src="https://github.com/user-attachments/assets/faf31c01-afcc-42cd-a937-85fe8771fb48" />


**Question 10**
---
<img width="724" height="450" alt="image" src="https://github.com/user-attachments/assets/272931fb-92d5-4a87-89d4-d252a4bb75c5" />


```sql
delete from Doctors
where doctor_id between 2 and 4;
```

**Output:**

<img width="1211" height="739" alt="image" src="https://github.com/user-attachments/assets/cf6d3014-292c-428c-ba73-9ced62f26822" />


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
