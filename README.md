# 22 - Component Lifecycle Methods

### The Component Lifecycle

Each component has several “lifecycle methods” that you can override to run code at particular times in the process. You can use this lifecycle diagram as a cheat sheet. In the list below, commonly used lifecycle methods are marked as bold. The rest of them exist for relatively rare use cases.

# Mounting
These methods are called in the following order when an instance of a component is being created and inserted into the DOM:

constructor()
static getDerivedStateFromProps()
render()
componentDidMount()

```
Note:  These methods are considered legacy and you should avoid them in new code:
-UNSAFE_componentWillMount()

```
# Updating
An update can be caused by changes to props or state. These methods are called in the following order when a component is being re-rendered:

static getDerivedStateFromProps()
shouldComponentUpdate()
render()
getSnapshotBeforeUpdate()
componentDidUpdate()

```
Note:

These methods are considered legacy and you should avoid them in new code:

UNSAFE_componentWillUpdate()
UNSAFE_componentWillReceiveProps()
```

# Unmounting
This method is called when a component is being removed from the DOM:

componentWillUnmount()
Error Handling
These methods are called when there is an error during rendering, in a lifecycle method, or in the constructor of any child component.

static getDerivedStateFromError()
componentDidCatch()
