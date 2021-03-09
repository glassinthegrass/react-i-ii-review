### Remember

Answer these on your own, then compare answers as a group

1.  What are props?
When React sees an element representing a user-defined component, it passes JSX attributes and children to this component as a single object. We call this object “props”.
-props is an object avail to the component 
-props are data being passed into a component 

2.  How do you pass props from a parent to a child?
they are accessible throught the parent. but rather than reference this you reference props
-we pass props into the child using the childs component tag 
-set up props on child components tag by saying <whateverPropertyName>=<hardcodedDataOrReferenceToExistingDataUsingCurlyBraces/>
3.  How do you access props from a class based child component?
from within JSX- {this.props.propName} and outside JSX
4.  How do you access props from a functional component?
-props.propName
5.  How do you bind a function to a parent component so that it can be passed to a child?
1) from within the constructor outside the state and before the methods <function name> = this.<function name>.bind.this
use lexical binding by not using the bind method and using the => functions

### Understand

Discuss this question in pairs if you have a 4-person group

6.  What's happening in this component?

```jsx
import React, { Component } from "react";

class Queue extends Component {
  constructor(props) {
    super(props);

    this.state = {
      questions: []
    };

    this.askQuestion = this.askQuestion.bind(this);
    this.answerQuestion = this.answerQuestion.bind(this);
  }
  askQuestion(newQuestion) {
    const questions = [...this.state.questions, newQuestion];
    this.setState({ questions });
  }
  answerQuestion(index) {
    const questions = [...this.state.questions];
    questions.splice(index, 1);
    this.setState({ questions });
  }
  render() {
    return (
    <div className="queue-container">
      <h1>The Queue</h1>
      <h3>{this.state.questions.length}</h3>
      <h3>questions need answers</h3>
      <Student askQuestion={this.askQuestion} />
      <Mentor answerQuestion={this.answerQuestion} />
    </div>;
  
  )
  }
}
```
-WE are passing down seperate 
### Apply

Try these on your own, but work together if you start to get stuck.

7.  Using the `Queue` component above, create a `Student` component that can add a question as a string and a `Mentor` component that can remove a question from the array.

### Analyze, Evaluate, Create

Discuss these questions as a group

8.  In the Queue component above, why are we holding state in the Queue component instead of Mentor or Student?
