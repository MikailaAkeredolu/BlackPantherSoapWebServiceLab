 #	Black Panther Soap WebService

 ### Objectives
Students will practice creating a soap web service in this lab.

After completing this lab students should be familiar with creating a soap API with CRUD functionalities.

 ### Overview
In this lab you will practice creating a simple Web service (contract first approach) designed to make use of SOA Architecture.


Generate a spring intialzr project via start.spring.io

Hint: Add the following maven dependencies JPA, Web Services and H2

 ### Instructions

 #### Part 1:
Create a xsd file to  addActorRequest, getActorByIdRequest, updateActorRequest, getAllActorsRequest and deleteActorRequest.
Hint: Add the corresponding responses too to your schema definition file (xsd)


In your database each actor should have an Id, name and a description

Example:  
```
Id: 1
```
```
Name: 	Chadwick Boseman
```
```
Description: T'Challa / Black Panther
```


Once you are done. Create files for your WebService Configuration, endpoints, repository, service and entity in seperate packages.

 #### Part 2:
Connect your soap web service to the h2 in memory database
Add your top 5 Black Panther Actors to to your databse via your web service and ensure all CRUD functionalities work. 

 #### Part 3:
Add a service status to output success and failure with the following CRUD operations. Create Update, DELETE #wakandaforever

Example

```
 <ns2:statusCode>SUCCESS</ns2:statusCode>
 <ns2:message>Actor Updated Successfully</ns2:message>
       
```

```
 <ns2:statusCode>SUCCESS</ns2:statusCode>
 <ns2:message>Actor Added Successfully</ns2:message>
 
```

```
 <ns2:statusCode>SUCCESS</ns2:statusCode>
 <ns2:message>Actor Deleted Successfully</ns2:message>
```




