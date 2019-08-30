# JavaScript

## Array

### unshift
Add items at the beginning of the array.
``` js
persons = [ 'Brendan Eich' ]
persons.unshift( 'Ryan Dahl' )
console.log( persons )
[ 'Ryan Dahl', 'Brendan Eich' ]
```

### push
Add items at the end of the array
``` js
persons = [ 'Ryan Dahl', 'Brendan Eich' ]
persons.push( 'Evan You' )
console.log( persons )
[ 'Ryan Dahl', 'Brendan Eich', 'Evan You' ]
```

## Arrow function
``` js
const foo = function foo() {
  console.log( 'function foo' )
}
foo()
function foo

const bar = () => {
  console.log( 'arrow function bar' )
}
bar()
arrow function bar

const fooBar = () => console.log( 'arrow one-liner' )
fooBar()
arrow one-liner
```

## Class
``` js
class Game {
  constructor( name, developer, console ) {
    this.name      = name
    this.developer = developer
    this.console   = console
  }
}

const game = new Game( 'The Last of Us', 'Naughty Dog', 'PlayStation' )
console.log( game )
Game { name: 'The Last of Us', developer: 'Naughty Dog', console: 'PlayStation' }
```

## Destructuring
``` js
const person = {
  name: 'John Doe',
  social: {
    email: 'johndoe@mail.com',
    twitter: '@johndoe'
  }
}

const { email, twitter } = person.social
console.log( `email: ${ email }, twitter: ${ twitter }` )
email: johndoe@mail.com, twitter: @johndoe
```

## Filter
``` js
const animals = [
  { name: 'Fluffy',   species: 'Rabbit' },
  { name: 'Caro',     species: 'Dog' },
  { name: 'Harold',   species: 'Fish' },
  { name: 'Sammy',    species: 'Cat' },
  { name: 'Hamilton', species: 'Dog' }
]

const dogs = animals.filter( animal => animal.species === 'Dog' )
console.log( dogs )
[ { name: 'Caro', species: 'Dog' }, { name: 'Hamilton', species: 'Dog' } ]
```

## Find
``` js
const things = [
  { id: '1', title: 'Get groceries', category: 'Inbox' },
  { id: '2', title: 'Walk the dog',  category: 'Today' },
  { id: '3', title: 'Maw the lawn',  category: 'Inbox' }
]
const thing = things.find( thing => thing.id === '2' )
console.log( thing.title )
Walk the dog
```

## Hoisting
``` js
hello()
// Function declaration is hoisted
function hello(){
  console.log( 'Hello World' )
}

// Function expression is not hoisted
const message = function(){
  console.log( 'Message' )
}
message()
Hello World
Message
```

## Loops
For statement
``` js
const names = [ 'Yoshi', 'Mario', 'Luigi' ]
for( let i = 0; i < names.length; i++ ){
  console.log( names[i] )
}
Yoshi
Mario
Luigi
```

## Map
``` js
fruits = [
  { id: 205, name: 'Banana', price: 30 },
  { id: 206, name: 'Apple',  price: 15 },
  { id: 207, name: 'Pear',   price: 25 }
]

const yummy = fruits.map( fruit => fruit.name )
console.log( yummy )
[ 'Banana', 'Apple', 'Pear' ]
```

## Rest
``` js
const rest = ( ...args ) => console.log( ...args )
rest( 'dude', 'where', 'is', 'my', 'car' )
dude where is my car
```

## Spread
``` js
const games = [ 'Halo', 'Uncharted', 'GTA', 'Dark Souls', 'Zelda' ]
const game  = 'The Last of Us'

const collection = [ ...games, game ]
console.log( collection )
[ 'Halo',
  'Uncharted',
  'GTA',
  'Dark Souls',
  'Zelda',
  'The Last of Us' ]
```