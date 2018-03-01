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
Create a xsd file for the following endpoints
 - addActorRequest
 - getActorByIdRequest
 - updateActorRequest
 - getAllActorsRequest
 - deleteActorRequest.

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
- Connect your soap web service to the h2 in memory database (Bonus points if you use Mysql)
- Download and Install Soap UI
- Use Soap UI to add your top 5 Black Panther Actors to to your database via your web service and ensure all C.R.U.D functionalities work. 

Example
- Request
```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:art="http://mikailapages.com/article-ws">
   <soapenv:Header/>
   <soapenv:Body>
      <art:addArticleRequest>
         <art:title>Soap Request</art:title>
         <art:category>Soap UI Request demo</art:category>
      </art:addArticleRequest>
   </soapenv:Body>
</soapenv:Envelope>
```
- Response
```
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/">
   <SOAP-ENV:Header/>
   <SOAP-ENV:Body>
      <ns2:addArticleResponse xmlns:ns2="http://mikailapages.com/article-ws">
         <ns2:serviceStatus>
            <ns2:statusCode>SUCCESS</ns2:statusCode>
            <ns2:message>Content Added Successfully</ns2:message>
         </ns2:serviceStatus>
         <ns2:articleInfo>
            <ns2:articleId>6</ns2:articleId>
            <ns2:title>Soap Request</ns2:title>
            <ns2:category>Soap UI Request demo</ns2:category>
         </ns2:articleInfo>
      </ns2:addArticleResponse>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```
 #### Part 3:
Add a service status to output success and failure with the following CRUD operations. Create Update, DELETE 

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



- #wakandaforever
