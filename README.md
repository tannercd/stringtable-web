# String Table
This small project was apart of a JavaScript curriculumn created by Jad Joubran. I gave this String Variation table my own spin and got familiar with Node and ESLint for code analysis in the process.

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

#### Clone Repo (Quickstart)

```
git clone https://github.com/tannercd/stringtable-web.git
```

### Prerequisites
1. Node.js (https://nodejs.org/en/)
2. ESLint (https://eslint.org/)

To run this project you will need Node.js installed (use link above) then we can use `npm` to globally install ESLint.

* With Node and Node.js installed:
```
npm install eslint -g
```

### Installing

* Fork this repo and run the application on any local server to test the String table.

* You can view this application publicly through my Pen (https://codepen.io/spherical/pen/KKdRBmr).

<img width="575" alt="Screen Shot 2020-05-11 at 4 43 00 PM" src="https://user-images.githubusercontent.com/48612525/81622693-9280f300-93a6-11ea-9cef-2d0bde30dbe8.png">


### Coding style tests

This project is using ESLint as a static code analyis tool for finding problematic patterns in JavaScript code. 

* Current Default ESLint Rules: (JSON Format)

```
"rules": {
  "indent": [
	  "error",
	  2
  ],
  "linebreak-style": [
	  "error",
	  "unix"
  ],
  "quotes": [
	  "error",
	  "double"
  ],
  "semi": [
	  "error",
	  "always"
  ]
}
```

Here is an example of a "problematic" code block that can benefit from linting with my projects ESLint rules. For the sake of this example, imagine the code below resides within `test.js`.

```
const myMessage = 'Hello World'

function sendMessage(message) {
    console.log(message);
}

myMessae("hello world");
```

There are many problems that ESLint will notify for the above code snippet based on the rules defined, strings must use double quotes, must use semi-colons etc. Below are the errors created from running `eslist test.js` inside my Visual Studio Code terminal:

```
spherical:strings-project TannerDolby$ eslint test.js

/Applications/MAMP/htdocs/strings-project/test.js
  1:7   error  'myMessage' is assigned a value but never used  no-unused-vars
  1:19  error  Strings must use doublequote                    quotes
  3:10  error  'sendMessage' is defined but never used         no-unused-vars
  7:1   error  'sendMesage' is not defined                     no-undef

✖ 4 problems (4 errors, 0 warnings)
  1 error and 0 warnings potentially fixable with the `--fix` option.

```

To use the power of ESLint for code analysis on any JavaScript file. Open a terminal or bash and run: `eslint filename.js` or with npm: `npm run lint`.

## Deployment
No need for live deployment, as its a small example app showcasing common string variations.

## Built With
* Node - JavaScript runtime for Server side JS
* JavaScript - Client side JavaScript
* HTML - Used to structure DOM and organize page content
* CSS - The styling sheet for DOM elements
* ESLint - Used for static code analysis

## Contributing
Please use proper contributing etiquette for submitting a pull request to this repo. I'm happy to fix my mistakes if you help me find them!

## Acknowledgments
A special thanks to Jad Joubran (@jadjoubran | https://github.com/jadjoubran) for providing the JavaScript course that helped me to modify this project to my liking. These interactive tables that serve populate table data on keyup are quite enjoyable to watch (and build).