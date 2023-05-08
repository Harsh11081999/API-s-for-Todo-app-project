# API-s-for-Todo-app-project
## MY LEADING CAMPUS INTERVIEW PROJECT 

**Prerequisites**

 * MySQL 

 * Node.js

**Setting up the Express server**

Now that we have our dependencies installed let's put them to work by first setting up our express server.

Create an app.js file and add the following code snippet below to it. We'll import the following:

* Express: To create our server.

* Cors: To allow and redirect request resources.

* Router: This is where our API routes will be defined later in the sections.

**Setup and connect to MySQL**

Now, we have our Express server set up. Let's go ahead and set up our MySQL
Next, execute the SQL statements  on your MySQL shell to create our todos database.

* CREATE DATABASE todos

Then, execute the command below to create our todolist table. The table will have an id, name, status, date_created  fields. The id filed will be the primary key of our table.

* CREATE TABLE todolist(id int NOT NULL AUTO_INCREMENT,
name varchar(50) NOT NULL, 
status varchar(50), 
date_created DATETIME DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP, 
PRIMARY KEY (id));

** Creating application controllers **

We have successfully connected our MySQL database. Let's proceed to create the routes for our application.

In our project root directory, create a controllers folder, then create an index.js file in the controllers folder.

Next, we'll create our createTodo handler to add new todos to our database. Then we check if the client is sending an empty form and return a 404 error message.

Then, we get the todo name from the request body and set the status of each todo created to pending by default. Using the query mysql method, we create an insert query to add the todo to our database.

## The routers used in project

* Get Route: to get all the todos in our database.
* Post Route: to add a new todo to our database
* Get Route: to get a todo by its id
* Put Route: to update a todo by the id
* Delete Route: to delete a todo by the id.












