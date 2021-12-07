## JSX

## React.createElement

creating a react element 
jsx: `const element = <h2 className='name'>Name</h2>`

to create a React element using the jsx element we use createElement

`const element = React.createElement( "h2", {
	className : 'name'
	}, 'Name')`

* jsx uses _className_ instead of _class_ to define css classes *

* Always start component names with capital letters *

## ReactDOM.render 

elements can be rendered into DOM using the _react-dom_ library 

```
function Example(props) {
	return (
	<h1> { props.name } </h1>
	<div className = "content">
		<p> { props.content } </p>
	</div>
	);
}

ReactDOM.render(
	<Tweet 
		name = "React"
		content = "A JS library for building user interfaces"
	/>,
	document.getElementById("root") )
// there needs to be a element with id 'root' where the tweet element renders

```

** most elements call ReactDOM.render(element, container) a single time to render the application **

## Two ways to create React component

1. Write a javascript function that returns either jsx or null

```
const SomeComponent = function() {
	return (
		<div className="customClass" />
		);
}
```

2. Other way is to define a React component with ES6 class syntax

```
class SomeComponent extends React.Component {
	constructor(props) {
		super(props);
	}
	
	render() {
	return ( <div className="customClass" />
		);
}
```

## Expressions in jsx

### Rule 1
All tags must be closed. two ways to close a tag
- use two tags `<div> ... </div>`
- use one self closing tag like ` <Example /> `

### Rule 2
Since we're creating a tree structure - a child tag must close before it's parent 

### Rule 3
All jsx expressions must result in one root level element. A function can only return one value.

### Rule 4
No HTML comments 
```
<!--- not allowed --->
{/*  this is good though */}
```


