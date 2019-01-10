# lareactcomponentcontextaccess
## 1.What's new
### 1 What's new react 16
list
- Improved sync rendering
- Returns arrays of elements
- Better error handling
- Small file size

## 2.Advanced Components
### 1 Compound components

```
React.Chilren.only(children)
```

## 3.Enhanced Components
### 1 Working with fragments
```
const nav = ()=>
<React.Fragment>
</React.Fragment>
```
same
```
const nav = ()=>
<>
</>
```
### 2 Using keyed fragments
```
{props.xx.dict.map(term=>(

<React.fragment key={}>
<>
)
```
### 3 Lifecycle
Render is called when the component is first mounted, but it's also called when new props come in or when Set State is called.
The mounting life cycle also includes the following: we have the constructor, this is called before the component is mounted and is a place to initialize state. We also have getDerivedStateFromProps in the mounting life cycle. This is invoked right after the component is constructed. And then finally we have component DidMount, which is called right after the component is mounted. This is a really good place to load data or make network requests.
We also have the UpdatingLifeCycle. This includes the following: now getDerivedStateFromProps we saw in the mounting life cycle, but it also fires when the component receives new props. shouldComponentUpdate if this returns false then Render and componentDidUpdate won't be called. We're gonna take a closer look at this one in particular in the next lesson. We also have render as part of the UpdatingLifeCycle also when the data changes, we call Render again. getSnapshotBeForeUpdate is going to be called right before the most recently rendered output is rendered.
Here we can't read the dom but we can capture a value for use later and then finally componentDidUpdate is invoked right after the update, so this can be used to operate on the dom once that update has occurred. Now the UnmountingLifeCycle only has one method on it and that is componentWillUnmount. This is invoked right before the component is unmounted and it's a great time to do some cleanup. You can cancel at request of the network, reset timers and all those types of clean up tasks.
So the react component life cycle has really undergone some change over time. We have new methods to make use of and all of these have to do with changes to Reacts handling of asynchronous information.

