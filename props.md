## React Props

Props in react is used to pass data between components 

Two ways of passing props 
- Pass as key value pairs

```
<Profile firstName="Amy" lastName= "Mansel" />
```

- Pass an object with spread operator { ...spread }

```
const user = { firstName = "Amy", lastName = "Mansel" }

<Profile {...user} />
```
