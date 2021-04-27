# **Netflix Clone using React.Js**

## **[useState](https://github.com/RgnDunes/Netflix-Clone#)**
This helps create a state variable inside a functional component.

```
Syntax :
const [messages, setMessages] = useState([{}]);
```

In above syntax *messages* is the name of state created. "setMessages" is a function that helps changing state just like setState in class component. The argument inside useState is the initial value of the state which in this case is a list of objects.

## **[useEffect](https://medium.com/trabe/react-useeffect-hook-44d8aa7cccd0)**
This function executes on a given condition.

```
Syntax :
useEffect(() => { setUsername(prompt('Please enter your name : ')); }, [])
```

Above function executes once because it's second argument is an empty list here. As long as we only want our effect (subscribe to resizes) to be called once, we pass an empty array as the second parameter of the function useEffect . An effect can optionally return a function (the cleanup function) that React will call when the component unmounts and before running the effect next time.

## **[axios](https://www.npmjs.com/package/react-axios)**
Axios is a library that helps us make http requests to external resources. In our React applications we often need to retrieve data from external APIs so it can be displayed in our web pages. ... After we retrieve the data, we typically add it to the state, so it's ready to be used by our application.

```
Syntax to create an axios instance
const axiosInstance = axios.create({
  baseURL: '/api/',
  timeout: 2000,
  headers: { 'X-Custom-Header': 'foobar' }
});
```
```
Syntax to make a call to the api :
axios.get('https://jsonplaceholder.typicode.com/posts').then(res => {
     this.setState({posts: res.data})
})
```

## **[async await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)**
> The "await" keyword is only valid inside "async" functions within regular JavaScript code. If you use it outside of an async function's body, you will get a SyntaxError.

> "await" can be used on its own with JavaScript modules.
```
General Syntax : 
async function name([param[, param[, ...param]]]) {
   statements
}
```
What **"await"** does is it says wait for the promise/answer to come back. async just makes a function asynchronous.
```
Syntax : 
useEffect(() => {
        async function fetchData() {
            const request = await axios.get(fetchUrl);
            return request;
        }
        fetchData();
    }, [])
```
An async function is a function declared with the async keyword, and the await keyword is permitted within them. The async and await keywords enable asynchronous, promise-based behavior to be written in a cleaner style, avoiding the need to explicitly configure promise chains.
>The purpose of async/await is to simplify the syntax necessary to consume promise-based APIs. The behavior of async/await is similar to combining generators and promises.
```
Normal Function : 
function resolveAfter2Seconds() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('resolved');
    }, 2000);
  });
}

Async Function : 
async function asyncCall() {
  console.log('calling');
  const result = await resolveAfter2Seconds();
  console.log(result);
  // expected output: "resolved"
}

asyncCall();

OR

async function foo() {
   return 1
}

...is equivalent to:

function foo() {
   return Promise.resolve(1)
}
```
> Async functions can contain zero or more await expressions. Await expressions make promise-returning functions behave as though they're synchronous by suspending execution until the returned promise is fulfilled or rejected. The resolved value of the promise is treated as the return value of the await expression. Use of async and await enables the use of ordinary try / catch blocks around asynchronous code.



## **[Firebase Commands Used](https://github.com/RgnDunes/Netflix-Clone#)**


## **[Firebase Deploy Commands](https://github.com/RgnDunes/Netflix-Clone#)**
- sudo npm install -g firebase-tools
- firebase login
- firebase init
- Hosting : Configure and deploy Firebase - Hosting sites
- Use an existing project
- Select your project
- What do you want to use as your public directory ? build
- Configure as a single page app ? Yes
- npm run build
- firebase deploy

#

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
