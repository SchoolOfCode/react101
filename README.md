# Context

> Context provides a way to pass data through the component tree without having to pass props down manually at every level.

Before hooks, there was [the original context API](https://reactjs.org/docs/context.html). Here you will find information on why context is useful as well as how to create a context and use it as a provider.

Since hooks came out, there's a much cleaner way to consume context with the [useContext](https://reactjs.org/docs/hooks-reference.html#usecontext) hook.

And as ususal, if you're still a bit confused, keep Googling - there are multitudes of guides online that explain how React's context API and useContext hook work, so find one that clicks with you.

Note: This workshop uses a library called parcel so that you can run each task separately in the same React app. For each task, run the appropriate script in the package.json, and view it at localhost:1234. (Example: For task one, run `npm run task1`.)

## Task 1

For this task, we will write all of our code in `task1/main.js`. Our goal is to create a context for the name value, provide that context to our entire app, and consume that context in our `GreatGrandchild` component

- create a context
- provide that context to the entire tree, and give it the value of your name.
- use the `useContext` hook to consume that context and read the value in the `GreatGrandchild`

**Bonus**

- In `App`, make the name value a piece of state, and create an input to change that state.

## Task 2

In task 2 we will be implementing a theme context and begin abstracting the context away into a nice pattern to work with. Task two has a more complex folder structure.

Begin by looking in `task2/themeContext.js`. You will find here a context provider component, as well as a context consumer hook. Take a few mins to read the code and ask yourself how you might use the two exported functions.

**The task...**

Your task is to provide the theme context to your entire component tree, and refactor each of the components to consume the style context.

## Task 3

Here will return to the infamous counter example. We will be creating our context and writing our provider component and consumer hook from scratch.

- Create your context in `task3/countContext.js`
- Export a provider component that will keep track of the count state and make it available in context, as well as a function to increment the count.
- Export a consumer hook that will allow you to access the count and the increment count function
- Provide the entire component tree with your context and refactor the appropriate components to use the `countContext` so that when the button is clicked, sheep are added!
