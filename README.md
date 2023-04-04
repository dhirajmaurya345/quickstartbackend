# quickstartbackend
This contains all context required to quickly start backend with mongo ,mongoose,express 

How to start a server
1. Install express - npm i express 
2. Require express in project -> create app.js file and use below code
   const express=require("express")
   const app=express()
3. You need a port number on which request can be processed 
   const port =3005;
4. Now we can listen on app with declared port number
   app.listen(port, () => {
   console.log("Server is running on port :", port);
   });
   
   now we run app.js file with node app.js and this will start our server; 

How to create simple get api with sample data

.....................................................................

Data modelling 
1. Different type of relation between data
2. Refrencing/normalization vs embedding/denormalization
3. Embeding or refrencing other documents?
4. Type of refrencing 


Relation between Data
1. one to one
2. one to many this is most importent that it further devided in 3 type
   1.  One to few
   2.  One to hundreds/thousands
   3.  One to millions  
3. Many to many

Key Notes for data modelling
1. The most important principle is : Structure your data to match the way your application queries and updates data
2. In other's word: Identify the question that arises from your application use cases first , and then model your data so that your question is answered in      the most efficient way ;
3. In general, always favour embedding, unless there is good reason not to embed. especiall to 1:few and 1:many relationship;
4. A 1:million or many:many is a good reason to refrence instead of refrencing;
5. Also, favor refrencing when data is updated a lot and if you frequently access a dataset on its own;
6. Use embeding when data is mostly read but rarely updated , and when two dataset belong intrinsically together;
7. Don't allow array to grow indefinitely. Therefor if you need to normalise, use child refrencing for 1:many relationships, and parent refrencing for            one:million relationship  
8. User two way refrencing for MANY:MANY
