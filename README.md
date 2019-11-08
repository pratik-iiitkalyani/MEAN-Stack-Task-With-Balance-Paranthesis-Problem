# MEAN-Stack-Task-With-Balance-Paranthesis-Problem

Node js/ Mongo DB Task.
1. Setup Node js with latest stable version. Pull out Mongo db with latest version.
2. Setup the Express  js and make the web server up.
3. Write up the Routes
4. Write up the controller logic and pass up data to service
5. Write up service and talk to mongo db for CRUD operations.
6. Use Postman to test the API's.
7. Please include the Read.Me file with API's you coded.
Register / Login with Balanced Parenthesis Operation API
1. API to do registration.  Please accept the registration data from user (email , password, DOB,username,role) and save them to MONGO DB. send back any error /success as response.
2. Implement the Login authentication with JWT. Accept username/password and ensure the jwt token generated and used to authenticate the CRUD API calls, if user not passing JWT token then you are not authorised message should come as response.
Once Login is successful , Send back the JWT token as {"token":xxxxxxx, message:"success"}
3. Once user successfully login with jwt token verified , Use this token and make a API call with route name (http://xx.x.x.x:PORT/balanced) which accepts the parenthesis as input. ( Ex: User passes {[]} as input and system should take this and perform  balanced or unbalanced paranthesis.
Sample :
{[] -> Unbalanced } is missing
{[]} -> balanced
({]}) -> unbalanced [  is missing
({[]}) -> balanced
So, Take this as input and perform the operation (Hint: Use Data structure) and return balanced or unbalanced to user. If balanced then save it to MONGO DB user defined "balanced" collection using his username and message as success . If same user calls this API again and again , increase the attempts variable in mongo DB by 1.
First call (http://xx.x.x.x:PORT/balanced) ->  failed to be balanced
: {username: xxxx  , message : , attempts : 1 } as response.
Second Call
(http://xx.x.x.x:PORT/balanced)   -> succed to be balanced
       : {username: xxxx  , message :Success , attempts : 2 }
4. Write an API to list all the registered users in DB (pass admin role JWT token)
5. Write an API to delete the registered user with admin login(pass admin role JWT token )
6. Expected clean and crispy code.
