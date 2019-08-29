# Spark-Collection

A Collection library for when arrays are not enough

## Installation

Install package with NPM :
```sh
npm install spark-collection
```

You can install it directly from github:
```sh
npm install kevthunder/spark-collection
```

## Usage

Include it in your script :
```js
const Collection = require ('spark-collection')
```

It accepts an array as a argument :
```js
const items = new Collection([1,2])
console.log(..items) // 1 2
```

Has function to add and remove unique items :
```js
const items = new Collection([1,2,3])
items.remove(2)
console.log(..items) // 1 3
items.add(4)
console.log(..items) // 1 3 4
items.add(4) // do nothing since it exists
console.log(..items) // 1 3 4
```

You can use any function from arrays and it will return a new Collection if needed :
```js
const items = new Collection([1,2,3,4])
const pair = items.filter( (item)=> item % 2 == 0 )
console.log(..pair) // 2 4
pair.add(6)
console.log(..pair) // 2 4 6
pair.pop()
console.log(..pair) // 2 4
```