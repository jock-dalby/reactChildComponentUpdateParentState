# reactChildComponentUpdateParentState

In this lesson, you'll be expanding on that pattern. The stateless, child component will update the state of the parent component.

Here's how that works:

Step1. The parent component class defines a function that calls this.setState.

Step2. Once the parent has defined a function that updates its state, the parent then passes that function down to a child.

Step3. The child receives the passed-down function, and uses it as an event handler.

See Parent.js and Child.js for examples

Take a look at changeName. You can see that it calls this.setState.

In order for changeName to work, the "this" in this.setState must be the instructions object of the Parent class. You're trying to set a <Parent />'s state, not some other type of component's state.

The meaning of this is determined when a function is called, not when when a function is defined. changeName is called by an event listener... on a <Child />. Shouldn't that make this point to the instructions object of the Child class, instead of the Parent class?

You'd think that it would! Fortunately it doesn't happen that way, thanks to some React magic called automatic binding.

Automatic binding allows you to pass functions as props, and any this values in the functions' bodies will automatically refer to whatever they referred to when the function was defined. No binding to worry about!
