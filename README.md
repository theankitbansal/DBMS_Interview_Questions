# DBMS_Interview_Questions

DBMS Basic Interview Questions


1. What is DBMS and what is its utility? Explain RDBMS with examples.

DBMS stands for Database Management System, is a set of applications or programs that enable users to create and maintain a database. DBMS provides a tool or an interface for performing various operations such as inserting, deleting, updating, etc. into a database. It is software that enables the storage of data more compactly and securely as compared to a file-based system.  A DBMS system helps a user to overcome problems like data inconsistency, data redundancy, etc. in a database and makes it more convenient and organized to use it.

Examples of popular DBMS systems are file systems, XML, Windows Registry, etc.

![image](https://user-images.githubusercontent.com/81725794/182896564-01f8be4e-987a-4ba0-bf82-6d9485230a6e.png)

RDBMS stands for Relational Database Management System and was introduced in the 1970s to access and store data more efficiently than DBMS. RDBMS stores data in the form of tables as compared to DBMS which stores data as files. Storing data as rows and columns makes it easier to locate specific values in the database and makes it more efficient as compared to DBMS.

Examples of popular RDBMS systems are MySQL, Oracle DB, etc.

2. What is a Database?

A Database is an organized, consistent, and logical collection of data that can easily be updated, accessed, and managed. Database mostly contains sets of tables or objects (anything created using create command is a database object) which consist of records and fields. A tuple or a row represents a single entry in a table. An attribute or a column represents the basic units of data storage, which contain information about a particular aspect of the table. DBMS extracts data from a database in the form of queries given by the user. 

3. Mention the issues with traditional file-based systems that make DBMS a better choice?

The absence of indexing in a traditional file-based system leaves us with the only option of scanning the full page and hence making the access of content tedious and super slow. The other issue is redundancy and inconsistency as files have many duplicate and redundant data and changing one of them makes all of them inconsistent. Accessing data is harder in traditional file-based systems because data is unorganized in them.

Another issue is the lack of concurrency control, which leads to one operation locking the entire page, as compared to DBMS where multiple operations can work on a single file simultaneously.

Integrity check, data isolation, atomicity, security, etc. are some other issues with traditional file-based systems for which DBMSs have provided some good solutions.

4. Explain a few advantages of a DBMS.

Following are the few advantages of using a DBMS. 

![image](https://user-images.githubusercontent.com/81725794/182896967-3d42ec14-fa4f-4375-ac21-4e7096ebbf43.png)

Data Sharing: Data from a single database can be simultaneously shared by multiple users. Such sharing also enables end-users to react to changes quickly in the database environment.

Integrity constraints: The existence of such constraints allows storing of data in an organized and refined manner.

Controlling redundancy in a database: Eliminates redundancy in a database by providing a mechanism that integrates all the data in a single database.

Data Independence: This allows changing the data structure without altering the composition of any of the executing application programs.

Provides backup and recovery facility: It can be configured to automatically create the backup of the data and restore the data in the database whenever required.

Data Security: DBMS provides the necessary tools to make the storage and transfer of data more reliable and secure. Authentication (the process of giving restricted access to a user) and encryption (encrypting sensitive data such as OTP, credit card information, etc.) are some popular tools used to secure data in a DBMS.

5. Explain different languages present in DBMS.

Following are various languages present in DBMS:

DDL(Data Definition Language):  It contains commands which are required to define the database.
E.g., CREATE, ALTER, DROP, TRUNCATE, RENAME, etc.

DML(Data Manipulation Language): It contains commands which are required to manipulate the data present in the database.
E.g., SELECT, UPDATE, INSERT, DELETE, etc.

DCL(Data Control Language):  It contains commands which are required to deal with the user permissions and controls of the database system.
E.g., GRANT and REVOKE.

TCL(Transaction Control Language):  It contains commands which are required to deal with the transaction of the database.
E.g., COMMIT, ROLLBACK, and SAVEPOINT.

6. What is meant by ACID properties in DBMS?

ACID stands for Atomicity, Consistency, Isolation, and Durability in a DBMS these are those properties that ensure a safe and secure way of sharing data among multiple users.

![image](https://user-images.githubusercontent.com/81725794/182897349-3c428929-f5d1-421a-b39f-6b1793994051.png)

1. Atomicity: This property reflects the concept of either executing the whole query or executing nothing at all, which implies that if an update occurs in a database then that update should either be reflected in the whole database or should not be reflected at all.

![image](https://user-images.githubusercontent.com/81725794/182897468-a3fb27b9-2733-4ac3-8b70-9fe1db9bde2a.png)

![image](https://user-images.githubusercontent.com/81725794/182897507-87ae470d-cee5-4f48-8e13-309debaafe03.png)

2. Consistency: This property ensures that the data remains consistent before and after a transaction in a database.

![image](https://user-images.githubusercontent.com/81725794/182897608-3a260dab-30cd-44a2-9c3a-a71335ab3eda.png)

3. Isolation: This property ensures that each transaction is occurring independently of the others. This implies that the state of an ongoing transaction doesn’t affect the state of another ongoing transaction.

![image](https://user-images.githubusercontent.com/81725794/182897727-c73b0902-8846-42b5-b0ca-44c910c697ad.png)

4. Durability: This property ensures that the data is not lost in cases of a system failure or restart and is present in the same state as it was before the system failure or restart.

7. Are NULL values in a database the same as that of blank space or zero?

No, a NULL value is very different from that of zero and blank space as it represents a value that is assigned, unknown, unavailable, or not applicable as compared to blank space which represents a character and zero represents a number.

Example: NULL value in “number_of_courses” taken by a student represents that its value is unknown whereas 0 in it means that the student hasn’t taken any courses.


Intermediate DBMS Interview Questions

8. What is Data Warehousing?

The process of collecting, extracting, transforming, and loading data from multiple sources and storing them in one database is known as data warehousing. A data warehouse can be considered as a central repository where data flows from transactional systems and other relational databases and is used for data analytics. A data warehouse comprises a wide variety of an organization’s historical data that supports the decision-making process in an organization.

![image](https://user-images.githubusercontent.com/81725794/182898630-e7cb7ec7-7580-4b6f-ad86-4df002cd1ad9.png)

9. Explain different levels of data abstraction in a DBMS.

The process of hiding irrelevant details from users is known as data abstraction. Data abstraction can be divided into 3 levels:

![image](https://user-images.githubusercontent.com/81725794/182898740-24172389-2a7f-416f-b2be-c56997fb6e5f.png)

Physical Level:  it is the lowest level and is managed by DBMS. This level consists of data storage descriptions and the details of this level are typically hidden from system admins, developers, and users.

Conceptual or Logical level:  it is the level on which developers and system admins work and it determines what data is stored in the database and what is the relationship between the data points.

External or View level: it is the level that describes only part of the database and hides the details of the table schema and its physical storage from the users. The result of a query is an example of View level data abstraction.  A view is a virtual table created by selecting fields from one or more tables present in the database.

10. What is meant by an entity-relationship (E-R) model? Explain the terms Entity, Entity Type, and Entity Set in DBMS.

An entity-relationship model is a diagrammatic approach to a database design where real-world objects are represented as entities and relationships between them are mentioned.

![image](https://user-images.githubusercontent.com/81725794/182898973-a71f9805-d494-4305-84ea-3b3aea9b8761.png)

Entity: An entity is defined as a real-world object having attributes that represent characteristics of that particular object. For example, a student, an employee, or a teacher represents an entity.
Entity Type: An entity type is defined as a collection of entities that have the same attributes. One or more related tables in a database represent an entity type. Entity type or attributes can be understood as a characteristic which uniquely identifies the entity.  For example, a student represents an entity that has attributes such as student_id, student_name, etc.
Entity Set: An entity set can be defined as a set of all the entities present in a specific entity type in a database. For example, a set of all the students, employees, teachers, etc. represent an entity set.

11. Explain different types of relationships amongst tables in a DBMS.

Following are different types of relationship amongst tables in a DBMS system:

1. One to One Relationship:  This type of relationship is applied when a particular row in table X is linked to a singular row in table Y.

![image](https://user-images.githubusercontent.com/81725794/182899136-deca7ea6-a395-42c6-a4a8-1c166acc137e.png)

2. One to Many Relationship: This type of relationship is applied when a single row in table X is related to many rows in table Y.

![image](https://user-images.githubusercontent.com/81725794/182899274-7fa583d8-e2d5-4f46-8bc1-fe61a7b4efbc.png)

3. Many to Many Relationship: This type of relationship is applied when multiple rows in table X can be linked to multiple rows in table Y.

![image](https://user-images.githubusercontent.com/81725794/182899373-b07a0fb6-9dfb-49d1-ae80-947fe9e4f5af.png)

4. Self Referencing Relationship: This type of relationship is applied when a particular row in table X is associated with the same table.

![image](https://user-images.githubusercontent.com/81725794/182899454-04f1fac0-a39b-4e51-9522-d790d9d588b5.png)

12. Explain the difference between intension and extension in a database.

Following is the major difference between intension and extension in a database:

Intension: Intension or popularly known as database schema is used to define the description of the database and is specified during the design of the database and mostly remains unchanged.

Extension: Extension on the other hand is the measure of the number of tuples present in the database at any given point in time. The extension of a database is also referred to as the snapshot of the database and its value keeps changing as and when the tuples are created, updated, or destroyed in a database.

13. Explain the difference between the DELETE and TRUNCATE command in a DBMS.

DELETE command: this command is needed to delete rows from a table based on the condition provided by the WHERE clause.

It deletes only the rows which are specified by the WHERE clause.
It can be rolled back if required.
It maintains a log to lock the row of the table before deleting it and hence it’s slow.

TRUNCATE command: this command is needed to remove complete data from a table in a database. It is like a DELETE command which has no WHERE clause.

It removes complete data from a table in a database.
It can be rolled back even if required. ( truncate can be rolled back in some databases depending on their version but it can be tricky and can lead to data loss). Check this link for more details
It doesn’t maintain a log and deletes the whole table at once and hence it’s fast.

14. What is a lock. Explain the major difference between a shared lock and an exclusive lock during a transaction in a database.

A database lock is a mechanism to protect a shared piece of data from getting updated by two or more database users at the same time. When a single database user or session has acquired a lock then no other database user or session can modify that data until the lock is released.

Shared Lock: A shared lock is required for reading a data item and many transactions may hold a lock on the same data item in a shared lock. Multiple transactions are allowed to read the data items in a shared lock.
Exclusive lock: An exclusive lock is a lock on any transaction that is about to perform a write operation. This type of lock doesn’t allow more than one transaction and hence prevents any inconsistency in the database. 

15. What is meant by normalization and denormalization?

Normalization is a process of reducing redundancy by organizing the data into multiple tables. Normalization leads to better usage of disk spaces and makes it easier to maintain the integrity of the database.  

Denormalization is the reverse process of normalization as it combines the tables which have been normalized into a single table so that data retrieval becomes faster. JOIN operation allows us to create a denormalized form of the data by reversing the normalization. 

Advanced DBMS Interview Questions

16. Explain different types of Normalization forms in a DBMS.

Following are the major normalization forms in a DBMS:

![image](https://user-images.githubusercontent.com/81725794/183000489-2d9bad78-82bc-4db9-981c-52d7107d2529.png)

![image](https://user-images.githubusercontent.com/81725794/183000511-90f4aa71-6fe3-4060-b06d-b0fcd6dc4dd6.png)

Considering the above Table-1 as the reference example for understanding different normalization forms.

1NF: It is known as the first normal form and is the simplest type of normalization that you can implement in a database. A table to be in its first normal form should satisfy the following conditions:
Every column must have a single value and should be atomic.
Duplicate columns from the same table should be removed.
Separate tables should be created for each group of related data and each row should be identified with a unique column.

![image](https://user-images.githubusercontent.com/81725794/183000535-fbda5fa5-b4b6-4b33-a711-4cf2ec686be8.png)

Table-1 converted to 1NF form

2NF: It is known as the second normal form. A table to be in its second normal form should satisfy the following conditions:
The table should be in its 1NF i.e. satisfy all the conditions of 1NF.
Every non-prime attribute of the table should be fully functionally dependent on the primary key i.e. every non-key attribute should be dependent on the primary key in such a way that if any key element is deleted then even the non_key element will be saved in the database.

![image](https://user-images.githubusercontent.com/81725794/183000586-04cfeb14-0929-4543-93a9-ca339a25a620.png)

![image](https://user-images.githubusercontent.com/81725794/183000619-2ea71340-2d65-4ef5-9433-64dc098b3933.png)

Breaking Table-1 into 2 different tables to move it to 2NF.

3NF: It is known as the third normal form. A table to be in its second normal form should satisfy the following conditions:
The table should be in its 2NF i.e. satisfy all the conditions of 2NF.
There is no transitive functional dependency of one attribute on any attribute in the same table.

![image](https://user-images.githubusercontent.com/81725794/183000641-3662f288-6544-4d9f-866a-58f042987d7d.png)

![image](https://user-images.githubusercontent.com/81725794/183000643-5fd46bcd-0b77-4718-9334-fb0c51af0d96.png)

![image](https://user-images.githubusercontent.com/81725794/183000660-a12fb6c8-aca6-4a46-a0e0-8f179bf5a8d4.png)

Breaking Table-1 into 3 different tables to move it to 3NF. 

BCNF: BCNF stands for Boyce-Codd Normal Form and is an advanced form of 3NF. It is also referred to as 3.5NF for the same reason. A table to be in its BCNF normal form should satisfy the following conditions:
The table should be in its 3NF i.e. satisfy all the conditions of 3NF.
For every functional dependency of any attribute A on B
(A->B), A should be the super key of the table. It simply implies that A can’t be a non-prime attribute if B is a prime attribute.

17. Explain different types of keys in a database.

There are mainly 7 types of keys in a database:

Candidate Key: The candidate key represents a set of properties that can uniquely identify a table. Each table may have multiple candidate keys. One key amongst all candidate keys can be chosen as a primary key. In the below example since studentId and firstName can be considered as a Candidate Key since they can uniquely identify every tuple.
Super Key: The super key defines a set of attributes that can uniquely identify a tuple. Candidate key and primary key are subsets of the super key, in other words, the super key is their superset.

![image](https://user-images.githubusercontent.com/81725794/183000706-b12b954a-062b-484a-aed0-bb75a99d31f9.png)

Primary Key: The primary key defines a set of attributes that are used to uniquely identify every tuple. In the below example studentId and firstName are candidate keys and any one of them can be chosen as a Primary Key. In the given example studentId is chosen as the primary key for the student table.

Unique Key: The unique key is very similar to the primary key except that primary keys don’t allow NULL values in the column but unique keys allow them. So essentially unique keys are primary keys with NULL values.

Alternate Key: All the candidate keys which are not chosen as primary keys are considered as alternate Keys. In the below example, firstname and lastname are alternate keys in the database.

Foreign Key:  The foreign key defines an attribute that can only take the values present in one table common to the attribute present in another table. In the below example courseId from the Student table is a foreign key to the Course table, as both, the tables contain courseId as one of their attributes.

Composite Key:  A composite key refers to a combination of two or more columns that can uniquely identify each tuple in a table. In the below example the studentId and firstname can be grouped to uniquely identify every tuple in the table.

![image](https://user-images.githubusercontent.com/81725794/183000746-2b0ccb02-576e-4134-892c-52db0650b4c8.png)

18. Explain the difference between a 2-tier and 3-tier architecture in a DBMS.

The 2-tier architecture refers to the client-server architecture in which applications at the client end directly communicate with the database at the server end without any middleware involved.
Example – Contact Management System created using MS-Access or Railway Reservation System, etc.

![image](https://user-images.githubusercontent.com/81725794/183000803-6f55da92-ce65-4a14-b24f-e9ef8c59413e.png)

The above picture represents a 2-tier architecture in a DBMS.

The 3-tier architecture contains another layer between the client and the server to provide GUI to the users and make the system much more secure and accessible. In this type of architecture, the application present on the client end interacts with an application on the server end which further communicates with the database system.

Example – Designing registration form which contains a text box, label, button or a large website on the Internet, etc.

![image](https://user-images.githubusercontent.com/81725794/183000826-8b58f67d-ebf1-46a2-b5b3-79de6def368e.png)

The above picture represents a 3-tier architecture in a DBMS.

