//-----------------------------Node-Day1-----------------------//

1.What is node.js ?
ans:
Node.js is an open-source server side runtime environment built on Chrome's V8 JavaScript engine. It provides an event driven, non-blocking (asynchronous) I/O and cross-platform runtime environment for building highly scalable server-side applications using JavaScript.
=================================================================
2.What is NPM?

1]The name npm (Node Package Manager) stems from when npm first was created as a package manager for Node.js.

2]All npm packages are defined in files called package.json.

3]The content of package.json must be written in JSON.

🎉At least two fields must be present in the definition file: name and version.

4]npm can manage dependencies.

5]npm can (in one command line) install all the dependencies of a project.

6]Dependencies are also defined in package.json.

==================================================================
3.What are the different modules in Node.js?
ans:
In Node.js Application, a Module can be considered as a block of code that provide a simple or complex functionality that can communicate with external application. 

Modules can be organized in a single file or a collection of multiple files/folders. 

Almost all programmers prefer modules because of their reusability throughout the application and ability to reduce the complexity of code into smaller pieces. 

Nodejs uses the CommonJS Module standard implementation in its module ecosystem. 

Types of Modules:  In Nodejs, there is 3 type of modules namely

🎉Core Modules
🎉Local Modules 
🎉Third-Party Modules


1.Core Modules:  Node.js comes with dozens of built-in modules. These built-in modules are sometimes referred to as core modules.

2.Local Modules: Putting all your code in a single file is not a good idea. As you add more code, you’ll want to stay organized and break your Node.js app into multiple scripts that all work together. For that purpose, we can create local modules in our application. 


3.Third-party Modules:  Third-party modules can be installed from the NPM (Node Package Manager) available online. 

Examples of Third-Party Module: 

npm install express
npm install lodash
npm install mocha

=================================================================
4.What is the purpose of the module.exports?
ans:
The main purpose of module.exports is to achieve modular programming. Modular programming refers to separating the functionality of a program into independent, interchangeable modules, such that each contains everything necessary to execute only one aspect of the desired functionality.

=================================================================
5.Difference between default export and named export?
ans:
After adding first modules containing some functions to an application, there is a need to have a reliable way of accessing them.

First of all, the functions we should have access to should be exported from the file.

The easiest way to export function is to simply add export in front of it:

// user.js

export const fetchUsers = () => {
  ...
};


There is another type of export that is only allowed once per file - default export:

// project.js

export default () => {
  ...
};

For default export, it is possible to export only a single value per file.
==================================================================
6.How do you import any module in Node.js
ans:
Importing a Module: We need to import the module to use the functions defined in the imported module in another file. The result returned by require() is stored in a variable which is used to invoke the functions using the dot notation.

// Importing the func.js module

// The ./ says that the func module
// is in the same directory as
// the main.js file
const f = require('./func');

// Require returns an object with add()
// and stores it in the f variable
// which is used to invoke the required

const result = f.add(10, 5);

console.log('The result is:', result);
==================================================================