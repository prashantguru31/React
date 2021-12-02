# React
**Lifecycle Methods List**

The following methods are called when a component is being added to the DOM:

**constructor() :** called before component is mounted. NEVER put side effect code inside of the constructor. Use ComponentDidMount for that instead. Commonly used to initialize state or bind methods. 

**componentWillMount():** invoked immediately before mounting occurs. Called before render. Once again, DO NOT put any side effect code inside of componentWillMount, and do not make API calls in this method  

**render():** never fetch data inside of render. Should only be used to return elements.

**componentDidMount():** Perfect place to fetch data. It gets called after render. This makes it clear that the initial state is empty at first, until we fetch it and re-trigger render. This forces us to set up our initial state properly, otherwise you're likely to get undefined states.
