> Please help us improve and share your feedback! If you find better tutorials or links, please share them by opening a Pull Request.

# HackYourFuture Node.js - Homework week 3

## Assignment:
1. Simple HTTP Server:
	Create an http server that can add and subtract from a number, which we will call the "state". Please see in `index.js` in this folder as starting material. Pay extra attention to line 21, which contains some hints for this week `console.log('New http request received', request.url);`

	**Rule 1**: DO NOT USE EXPRESS.JS

	**Rule 2**: you can use other packages, but you HAVE to also make a version WITHOUT any NPM packages (http, of course, is not NPM but a node native package)

	```js
	// The state
	var state = 10; 
	```

	Endpoints criteria
	```js
	// /state 
	// response: the current state in a html format 
	// when the server starts, this should return "10"
	http://localhost:8080/state 

	// /add
	// Response: "ok" in html format
	// This should add 1 to the current state
	http://localhost:8080/add

	// /remove
	// Response: "ok" in html format
	// This should subtract 1 ƒrom the current state
	http://localhost:8080/remove

	// /reset
	// Response: "ok" in html format
	// This should set the state back to 10

	http://localhost:8080/reset

	// Any other URL
	// Response: return error code 404: Not found with a friendly message
	// and do not change the state variable
	http://localhost:8080/subtract
	```

2. Continuing on last week's homework:

	* Start from the [classwork folder](../classwork) folder.
	* Convert into a node project with `npm init`.
	* Add babel into the setup. (You can check if the setup is good if you can `import` instead of `require`, for example.) Reference: https://babeljs.io or [Marco's node-babel template](https://github.com/pmcalabrese/node-babel).
	* Make sure you have created `.babelrc` and `.gitignore` files, and added the scripts in `package.json` files.
	* Make a commit and push to Github at this stage.
	* Add more fields in the [form to add Contact](../classwork/public/index.html).
	* Handle the additional fields while constructing a `new Contact()`.
	* Add a method `/all-contacts` in your server to list all the contacts in the [JSON file](../classwork/src/contacts.json).
	* Create a new `contacts.html` file which uses the method above to render all contacts in a list. You could use `XMLHTTPRequest` or `fetch` that you have used previously to load data and `template strings` to render it.

## Reading

### Babel:
More about babel at https://babeljs.io/ and see the setup @pmcalabrese demonstrated in class at https://github.com/pmcalabrese/node-babel

### http, http listen
- Video basic: https://www.youtube.com/watch?v=pYOltVz7kL0
- Video routing: https://www.youtube.com/watch?v=_D2w0voFlEk (please focus on request.url, not request.method)
- Read: [Node JS documentation about http](https://nodejs.org/en/docs/guides/anatomy-of-an-http-transaction/)
- Read Advanced: 

While not strictly homework, we’ve created another playlist if you’d like to learn more or review (and as JavaScript developers, you should). https://www.lynda.com/SharedPlaylist/78e6513f51bb4102b03349460491b4e3
