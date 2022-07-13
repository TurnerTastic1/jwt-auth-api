# jwt-auth-api
My(Turner's) first API/project with JWT authentication using node and express. Built with help from bzkoder article that described how to build the app.
https://www.bezkoder.com/node-express-vue-jwt-auth/#Back-end_with_Nodejs_Express_038_Sequelize

## Operating instructions
- Clone repository and configure MySql database
- Run "node server.js" to start making calls through a tool like postman
- Reference for troubleshooting and database issues https://www.bezkoder.com/node-express-vue-jwt-auth/#Back-end_with_Nodejs_Express_038_Sequelize

## API documentation
* POST 
    * api/auth/signup
        * requires json obj like the following
        {
            "username": "user",
            "email": "user@test.com",
            "password": "12345678",
            "roles": ["role1", "role2"]
        }
        * returns: 200 ok - "message": "User registered successfully"
    * api/auth/signin
        * requires json obj like the following
        {
            "username": "mod",
            "password": "12345678"
        }
        * returns: 200 ok - user info and the accesstoken! 
        * Use the acccess token to use other API requests below
* GET
    * test/all
        * token is required - returns "public content"
    * test/user
        * token is required
    * test/mod
        * token is required
    * test/admin
        * token is required
## Credits and acknowledgments
[Reference](https://www.bezkoder.com/node-express-vue-jwt-auth/#Back-end_with_Nodejs_Express_038_Sequelize)

## News
Front end coming soon