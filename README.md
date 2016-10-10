# reactChildComponentUpdateParentState

In this lesson, you'll be expanding on that pattern. The stateless, child component will update the state of the parent component.

Here's how that works:

Step1. The parent component class defines a function that calls this.setState.

Step2. Once the parent has defined a function that updates its state, the parent then passes that function down to a child.

Step3. The child receives the passed-down function, and uses it as an event handler.
