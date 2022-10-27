# React Notes

## Components

In react, we compose complex UI's from isolated pieces of code called components
Components takes in parameter's called props and returns front end code to be displayed via the render method.

The front end code returned to be displayed is a React object though. Each react object is a javascript object that I can store in a variable

The react components are used in the render functions and they look like html tags 
ex: root.render(<Game />) -> this calls the game component

## Interactive Components and State

One way we can make our components interactive is by including a onClick function to a button we are rendering

Now that the component is interactive we can alter the state of component, but first we need to give the component state
We do this by adding a constructor to the component and setting this.state

### Lifting State

In our case we need to use the state from all the child squares to determine a winner of the game. 
we use super(props) in the constructor of the parent to get the state of the entire board. 

## Benefits of Immutability

We use slice to create a copy of the state array instead of modifying the existing array. This is an example of using immutability instead of mutability.

### Complex features are simplified
For example we implemented a "time travel" feature allowing us to undo moves. This is made much easier as the previous verisons of the game are still intact.

### Detecting Changes
We can easily detect changes by comparing the current state to our previous states that we have saved

### Determining when to re-render in React
The main benefit of immutability is that it allows us to build pure components in React. Immutable data can easily determine if changes have been made so we know to re-render

## Function Components

function components only contain a rend method and do not have any state. They still can take props as input like our Square function



## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!


### `npm run eject`