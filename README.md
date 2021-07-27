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
We use cors t o enable Cross origin resource sharing
To install cors module you need this command line:
`npm install cors --save`

