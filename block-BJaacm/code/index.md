```js
let user = {
  name: "Arya",
  sibling: ["Robb", "Ryan", "John"],
};
let allBrothers = ["Robb", "Ryan", "John"];
let brothersCopy = user.sibling;
let usename = user.name;
let newUser = user;
```

1. Memory representation

- Create the memory representation of the above snippet on notebook.
- Take a photo/screenshot and add it to the folder `code`

 ![name](./hello.jpg) 

2. Answer the following with reason:

- `user == newUser;` // true because the address of user and newUser is same.
- `user === newUser;`//true because the address of user and newUser is same.
- `user.name === newUser.name;`//true  because the address of user and newUser is same. 
- `user.name == newUser.name;`//true  because the address of user and newUser is same.
- `user.sibling == newUser.sibling;`//true  because the address of user and newUser is same.
- `user.sibling === newUser.sibling;`//true  because the address of user and newUser is same.
- `user.sibling == allBrothers;`//false because the value is changed.
- `user.sibling === allBrothers;`//false  because the value is changed.
- `brothersCopy === allBrothers;`//false
because the refrence point of sibling and brothersCopy is different.

- `brothersCopy == allBrothers;`//false
because the reference point of allBrothers and brothersCopy is different.


- `brothersCopy == user.sibling;`//false //false
because the reference point of allBrothers and brothersCopy is different.

- `brothersCopy === user.sibling;`
//true because the reference point is same
- `brothersCopy[0] === user.sibling[0];`
//true because the reference point is same.
- `brothersCopy[1] === user.sibling[1];`
//true because the reference point is same.
- `user.sibling[1] === newUser.sibling[1];`
//true because the refernce point is same.
