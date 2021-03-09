### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
-react is a  js library created and maintained by facebook
-used to manage the virtual DOM and create versatile and performant UI
-using component based architechture and unidirectional dataflow

2.  What is create-react-app?
create-react-app is a very basic react application provided by facebook so to provide a basic app for developers to learn in
-a package that sets up a new react project
-also sets up a developer server that will auto-refresh on changes
-npx is a package runner for npm

3.  What is Component Based Architecture?
component based architechture involves building seperate components on js documents filed under the components folder imported to the main app page and rendering there. components are highly versitile and reusable
-encapsulating individual pieces of code to bring together into a larger project/app

4.  What is JSX?
-jsx is the syntax extension of javascript facebook developed for react
-looks like html
-transpiled into regular JS function calls
-combines css html and js
-not unique to react

5.  What is the virtual DOM?
-lightweight copy of the actual DOM
-virtual dom is a representation of a ui that is live synced with a library like react to display your app
-when changes to component made the virtual dom informs the dom what actual changes need to be made

6.  What is unidirectional (one-way) data flow?
-data can only flow from parent to child and not the other direction
-parent to child using props
-ensures we have a single source of truth

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
it downloads a basic and predetermined version of react app to allow for quick developement rather than building from scratch each time
8.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

9.  Explain how data is passed from a parent component to a child component.

### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

14. Compare and contrast one-way data flow with two-way data binding.
