1. Write the output with reason

```js
const person = {
  firstName: 'John',
  lastName: 'Doe',
};

let person2 = person;

person.firstName = 'Arya';

console.log(person2.firstName); // Arya because person and person2 both are in same memory location.
console.log(person.firstName); // Arya because the value is changed to "Arya".
console.log(person.lastName); // Doe becuase the value is set to Doe.
console.log(person == person2); // true because person and person2 both are in same memory location
console.log(person === person2); // true because person and person2 both are in same memory location
console.log(person.lastName === person2.lastName); // true because person and person2 both are in same memory location
```

2. Write the output with reason:

```js
let person = {
  firstName: 'John',
  lastName: 'Doe',
  address: {
    street: 'North 1st',
    city: 'San Jose',
    state: 'CA',
    country: 'USA',
  },
};

let personTwo = { ...person };

person.firstName = 'Arya';
person.city = 'Navada';

console.log(personTwo.firstName); // John because we have cloned the values of first object into second one . However we are changing the values but no effect will occur in second object because it is saved in different memory location.
console.log(person.firstName); // Arya because the value is changed.
console.log(personTwo.lastName); // Doe because we have cloned the values of first object frm second one.
console.log(person.firstName === personTwo.firstName); // false because both the objects are not stored in same memory location.
console.log(person == personTwo); // false because both the objects are not stored in same memory location.
console.log(person === personTwo); // false because both the objects are not stored in same memory location.
console.log(person.address === personTwo.address); // true because both address objects are pointing to same memory location.
console.log(person.address == personTwo.address);//true because both address objects are pointing to same memory location. 
console.log(personTwo.address.city); // San Jose becuase here shallow cloning is done so it will copy the value.
console.log(person.address.city); // San Jose because the values are assigned .
console.log(person.address.city == personTwo.address.city);//true because in this case shallow cloning occured. So the values will be equal.
```

3. Write the output with reason:

```js
let person = {
  firstName: 'John',
  lastName: 'Doe',
  address: {
    street: 'North 1st',
    city: 'San Jose',
    state: 'CA',
    country: 'USA',
  },
};

let personTwo = { ...person, address: { ...person.address } };

person.firstName = 'Arya';
person.city = 'Navada';

console.log(personTwo.firstName); // John because we have cloned the values of person object to personTwo object.
console.log(person.firstName); //  Arya because the values are changed.
console.log(personTwo.lastName); // Doe because we have cloned the values of person object to personTwo object.
console.log(person.firstName === personTwo.firstName); // false becuase the name of the person is changed.
console.log(person == personTwo); // false becuase both the objects are stored in different memory location.
console.log(person === personTwo); // false becuase both the objects are stored in different memory location.
console.log(person.address === personTwo.address); // output
console.log(person.address == personTwo.address); //false because in this case we have done deep cloning so both addresses are pointing to different memory loactions.
console.log(personTwo.address.city); // San Jose because we have deep cloned values so the value will be same.
console.log(person.address.city); // San Jose because we have deep cloned values so the value will be same.
console.log(person.address.city == personTwo.address.city); // true 
```

4. Clone the `blogs` variable into a new variable named `clonedBlogs`

```js
let blogs = [
  {
    id: 1,
    title: 'Post #1',
    body: 'My first blog post',
  },
  {
    id: 2,
    title: 'Post #2',
    body: 'My second blog post',
  },
  {
    id: 3,
    title: 'Post #3',
    body: 'My third blog post',
  },
];

let clonedBlogs=[...blogs];
```

5. Clone the `question` variable into a new variable named `questionClone`

```js
var questions = [
  {
    prompt: 'Why is the sky blue?',
    responses: [
      'Because the color blue was on sale at Wallmart',
      'Because blue is the prettiest color',
      'Because the air molecules difract blue light more than any other color',
    ],
  },
  {
    prompt: 'Why are leaves usually green?',
    responses: [
      'So green caterpillars can hide better.',
      'Because leaves can more easily make energy with green light',
      "Because leaves absorb red and blue light so it's green that is reflected",
    ],
  },
];

let questionClone=[...questions];
console.log(questionClone);
```

6. Clone the `allBlogs` variable into a new variable named `allBlogsClone`

```js
var allBlogs = {
  id: 1,
  title: 'Alamofire JSON Serialization',
  body: 'All about serialization in Alamofire...',
  author: {
    id: 1,
    fullName: 'Jeff Potter',
    username: 'jpotts18',
  },
  comments: [
    {
      id: 1,
      body: 'Thanks for the help Jeff, this saved me hours',
    },
    {
      id: 2,
      body: 'Your welcome. I am happy to help!',
    },
  ],
};

let allBlogsClone={...allBlogs}
console.log(allBagsClone);
```

7. Clone the `person` variable into a new variable named `clonedPerson`

```js
let person = [
  {
    input: { name: 'Ryan' },
    output: { name: 'Ryan' },
  },
  {
    input: { name: { first: 'Ryan', last: 'Haskell-Glatz' } },
    output: { firstName: 'Ryan', lastName: 'Haskell-Glatz' },
  },
  {
    input: { name: 'Ryan', age: 24 },
    output: { name: 'Ryan', age: 24 },
  },
  {
    input: {
      name: { first: 'Ryan', last: 'Haskell-Glatz' },
      birthday: { year: 1993, month: 'Nov' },
    },
    output: {
      firstName: 'Ryan',
      lastName: 'Haskell-Glatz',
      birthdayYear: 1993,
      birthdayMonth: 'Nov',
    },
  },
];
let clonedPerson=[...person];
console.log(clonedPerson);
```

8. Write a function named `cloneObject` that accepts an object and returns the clone of the object

```js
function cloneObject(object) {
  return { ...object };
}
let user = {
  name: 'John',
  house: 'Stark',
  sisters: ['Arya', 'Sansa'],
};
let cloned = cloneObject(user);

let person = {
  firstName: 'John',
  lastName: 'Doe',
  address: {
    street: 'North 1st',
    city: 'San Jose',
    state: 'CA',
    country: 'USA',
  },
};

let clonedPerson = cloneObject(user);

console.log(
  `The user object is ${
    user == cloned ? `not clone` : `cloned successfully 😁👑`
  }`
);
console.log(
  `The person object is ${
    person == clonedPerson ? `not clone` : `cloned successfully 😁👑`
  }`
);
```
