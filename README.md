# membership-application

## Starting application

To start video-streamer application you need to run scrip: 

### `npm run development`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.\
Because this is back-end app there wont be much stuff on our page to actually see before we add front-end to our project.

## Developing Dependecies

To run backend backend application firstly we need to install and configurate some dependencies.

###  Babel

Because we will write backend code in ES6 we need babel to conver ES6.

### How to install babel

To install Babel modules you need to type this command line in terminal:

`npm install --save-dev babel-core babel-loader babel-preset-env babel-preset-stage-2`

**Dont forget to change version of babel-loader from 8.2.2 to 7.1.5**

###  Webpack

We will use webpack to compile and bundle our code using Babel

### How to install Webpack

To install Webpack modules you need to type this command line in terminal:

`npm install --save-dev webpack webpack-cli webpack-node-externals`

###  Nodemon

Because we want to restart node server when we update code we need Nodemon to monitor server code for changes.

### How to install Nodemon

To install Nodemon modules you need to type this command line in terminal:

`npm install --save-dev nodemon`

###  Express


### How to install Express

To install Express modules you need to type this command line in terminal:

`npm install express --save`

To handle HTTP request and send responses we will need following modules to configurate express:
1. ### body-parser
Body parser arse incoming request bodies in a middleware\
To install body-parser you need this command line:
`npm install body-parser --save`

2.  ### cookie-parser
Cookie-parser parsingmiddleware to parse and set cookies in request objects\
To install body-parser you need this command line:
`npm install cookie-parser --save`

3.  ### compression
Compression middlewere will attempt to compress response bodies for all requests goes through middlewere.
To install compression module you need this command line:
`npm install compression --save`

4.  ### helmet
Helmet is collection of middleware functions to help secure Express app by setting various HTTP headers
To install helmet module you need this command line:
`npm install helmet --save`

5.  ### cors
We use cors to enable Cross origin resource sharing
To install cors module you need this command line:
`npm install cors --save`

###  Mongoose

We will use moongose to connect our app on MongoDB and we will use Mongoose module to implement user model.

### How to install Mongoose

To install Mongoose you need to type this command line in terminal:

`npm install mongoose --save`

Url for conencting App with MongoDB is:
`mongodb://localhost:27017/mernproject`

###  Json Web Token

To enable functionality about authentification and authorization we need Json Web Token.

### How to install Json Web Token

To install Json Web Token you need to type this command line in terminal:

`npm install express-jwt jsonwebtoken --save`

## Testing

Because our app only have backend,somehow we need to test our CRUD operations. We will do it with Postman or any other app for API testing.\
If you want to to download Postman you can do it on this link [Postman](https://www.postman.com)

Currently in our application we can test this functionalites:

1. ### Listing all users
For this functionality we just need to GET all users with `/api/users/`\
If everything is OK we should get array of all users and their informations,but if something is wrong with code we should get error message.

2. ### Adding new user

We will add new user with POST method on `/api/users/` request.What we need to do before sending request is to add `key: Content-Type` and `value: application/json` in Header because we want to send json file to our app and to recive json file aswell.Then in Body we need to write information about our new user. We need to add name,email and password.
All 3 of them are required to create new user.If everything is good we should see message that we created new user, if not we will see error message.

**Note: You cant create user with same email**

3. ### Deleting user

To delete user we need DELETE method on `/api/users/:id` request.For this method we need id of user that we want to delete.If you forgot user id you can always get list of all users and see it again.One more thing,you can only delete your own account and to use this function you need to signin on our app otherwise you wont be able to delete user.If you try to delete other prifile you will get error.


4. ### Update user

Firstly you can only update your profile and to be able to update it you will need to be signed in app. If you are not then you wont be able to update user.If you are signed, you need PUT method on `/api/users/:id` request.In body you should write your new informations and send request.If everything went good your profile will be updated and if not you will see error message.If you try to update other prifile you will get error.

5. ### Get one user

Just like before you can get single user only if you are signed in on our application. To get single user you need to GET method on `/api/users/:id` request. You need to know your id. If everything went good you should see profile info with that id if not you will see error message.

5. ### Sign in

To sign in on this application you need to have your own profile.If you have it then you need to use POST method on `/auth/signin` request.In body you should write your email and password, if everything is good you should get token in result.You need to copy that token and make new Header with `key: Authorization` and `value: Bearer + your token`.After that you will be able to delete update and get single user inforomation.


5. ### Sign out

To sign out you simple need to use GET method on `/auth/signout` request and you will be logged out if everything is good with code.
