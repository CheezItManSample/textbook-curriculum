# Creating Components: Part 2

## Learning Goals
- Continue nesting components within one another
- Continue practice component creation and JSX syntax

Next we are going to extend our application to support multiple students. Additionally, we are going to support components dynamically loading data.

## Load data from `props`

First, we want to use the Student component we already created, but we want to allow this to load data dynamically.

To do this, we will pass in the data from the App component to the Student component. Within the Student component, we will  use the code tags to pull in the data that was passed in.

1. Locate the spot where the `Student` component is rendered from the `App` component.

1. Update the component rendering to include two new parameters by adding them in like this:  
    - `<Student name="Improved Ada" email="improved-ada@ada.co" />`
    - This shouldn't change anything yet in our application, so save the file and refresh the browser to verify that the data still looks like the original hard-coded data.

1. Update the `render` function in the `Student` component to replace the hard-coded values with code tags `{ }` which contains the `prop` that came in from the parent component.  
  - It should now contain `{ this.props.name }` and `{ this.props.email }`
  - Verify that the content displayed is now coming from the values in the `App` component.
  - If you need to verify, take a look at [the code](https://github.com/AdaGold/react-hello-world/tree/part-3/src) so far.


If we identify each individual piece of the component rendered, we'll see:
![component prop breakdown](images/component-prop-breakdown.png)

Prop names can be any variable you want them to be. In this particular case, we chose `name` and `email` to store our values.

Once the prop names are **passed in** to the component, we can then use them within the component. That's where `this.props` comes in!

## Key Takeaway


## Additional Resources
- [How to write your first React component](https://medium.freecodecamp.org/how-to-write-your-first-react-js-component-d728d759cabc)