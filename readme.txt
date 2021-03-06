Pre-requisites
==============
1. Install Nodejs
2. Install MongoDB --- username:pwd    bhuvana_admin:bhuvana 


Procedure
===========
1. Download the project and open the folder in command line.
2. Type "npm install" to install the dependencies.
3. Type "npm serve" to run the application

Dependencies used
=================
bcrypt  3.0.5
body-parser  1.18.3
express  4.16.4
jsonwebtoken  8.5.1
mongoose  5.4.22
morgan  1.9.1
multer  1.4.1
rotating-file-stream  1.4.
nodemon  1.18.1 (Dev dependency)

Uses of dependencies
====================
bcrypt is used to create a hash for password taking password and number of hash rounds as input  
body-parser Parse incoming request bodies in a middleware
express is Node.js framework
jsonwebtoken is to generate a web token for the session
mongoose is ORM for Node.js and MongoDB. 
morgan for keeping logs during APIs. This can be found in log folder access.log file. It logs all the requests and errors. 
multer adds a body object and a file or files object to the request object.
rotating-file-stream is used for access.log file 
nodemon tool will develop node.js applications by automatically restarting the node application when file changes in the directory are detected.


About the project
=================
This is a project that takes in products and orders for the products. The user has to signup and login the add products and order for products. Each product takes input as name, price and product image. 
API's are written for Products, Orders and Users.

Products
========
get('/') List all products
post('/') Add a product  (Authorization required)
get('/:id') Get a product
patch('/:id') Update a product (Authorization required)
delete('/:id') Delete a product (Authorization required)

Orders
======
get('/') List all orders
get('/:id') Get an order
post('/') (Authorization required) Add an order
patch('/:id') (Authorization required) Update an order

Users
=====
post('/signup') Register/Signup user
get('/:id') Get user details
post('/login') Login user with email id and password as input. This generates a JWT which expires in 1day.
get('/') Get all users 
delete('/:id') (Authorization required) delete a user.

Upload
=======
Will contain product images that are uploaded during post operation.

Note
====
Output of each API can be seen through POSTMAN.
