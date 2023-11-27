1. What will be the output and explain the reason.

```js
let obj = { name: 'Arya' };
obj = { surname: 'Stark' };
let newObj = { name: 'Arya' };
let user = obj;
let arr = ['Hi'];
let arr2 = arr;
```

Answer the following with reason after going through the above code:

- `[10] === [10]`//false becuase they are stored at different locations in the memory
- What is the value of obj? // stark beacuse we have changes the value in line no 4
- `obj == newObj`//false because the values are different
- `obj === newObj`// false because the values are different
- `user === newObj`//false because the values are different
- `user == newObj`//false because the values are different
- `user == obj` //true because obj is assigned to newObj
- `arr == arr2` //true becuase both are stored in same memory location.
- `arr === arr2` //true because bith are stored in same memory location.

2. What's will be the value of `person1` and `person2` ? Explain with reason. Draw the memory representation diagram.

<!-- To add this image here use ![name](./hello.jpg) -->

```js
function personDetails(person) {
  person.age = 25;
  person = { name: 'John', age: 50 };
  return person;
}
var person1 = { name: 'Alex', age: 30 };
var person2 = personDetails(person1);
console.log(person1);//{ name: 'Alex', age: 25 } because the value of person is changed 

console.log(person2); //{ name: 'John', age: 50 }because the age is changed to 50
```

3. What will be the output of the below code:

```js
var brothers = ['Bran', 'John'];
var user = {
  name: 'Sansa',
};
user.brothers = brothers;
brothers.push('Robb');
console.log(user.brothers === brothers); //true because both brothers and user.brothers are stored in same memory location
console.log(user.brothers.length === brothers.length); //2.true becuase  both brothers and user.brothers are stored in same memory location so there length will be equal
```
