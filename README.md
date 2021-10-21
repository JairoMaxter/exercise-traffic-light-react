# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

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

### `yarn build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

# Traffic Light with React

Sometimes we want to create components with an internal state that changes overtime, imagine a traffic light that changes color every 3 seconds, for that we normally will make a variable color and set it to a default color:

```js
let color = "blue";
```

But we want our component to re-render and change the website HTML every time the variable color changes, that's why we use hooks:

```js
//        ↓ variable name             ↓ default value
const [ color, setColor] = useState("red");
//               ⬆ function to change the color
```

From now one, every time we use the function `setColor` to change the variable color, the component will re-render and the entire traffic light HTML will be updated with the new color. 

> You can [read more about hooks here](https://content.breatheco.de/lesson/react-hooks-explained).

## 🌱  How to start this project

Do not clone this repository.

The first step to start coding is cloning the [react boilerplate](https://github.com/4GeeksAcademy/react-hello) on your local computer or gitpod.

a) If using Gitpod (recommended) you can clone the boilerplate by [clicking here](https://github.com/4GeeksAcademy/react-hello).

b) If working locally type the following command from your command line: `$ git clone https://github.com/4GeeksAcademy/react-hello`.

💡 Important: Remember to create a new repository, update the remote (`git remote set-url origin <your new url>`), and upload the code to your new repository using `add`, `commit` and `push`.

## 📝 Instructions

Let's simulate a traffic light [like this one](https://github.com/breatheco-de/exercise-traffic-light-react/blob/master/preview.gif).

The light has to glow when clicked.

- The whole purpose of the component is displaying a traffic light with red, yellow and green lights.
- When any light is clicked (selected) it has to glow, but the other lights have to stop glowing.
- The component must have a hooked state variable that tracks the color:

```js
const [ color, setColor] = useState("red");
```

- Use the setColor function to change the color an the component will automatically re-render (because it's hooked with `useState`).

- Use the ReactDOM.render to render the component into the DOM like this
```js
ReactDOM.render(<TrafficLight />, document.querySelector('#app'));
```