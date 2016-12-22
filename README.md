# Introduction to ES6 Quiz

## Objectives

1. Test your understanding of ES6 syntax
2. Review Javascript principles

???

# ES6 Quiz

?: `var` declares a block-scoped variable

( ) True
(x) False

?: `const` declares a block-scoped variable

(x) True
( ) False

?: `let` declares a block-scoped variable

(x) True
( ) False

?: What is the final value of `obj` in the following example?

```javascript
const obj = { foo: 1 }

obj.bar = 2
```

( ) `{ foo: 1 }`
( ) N/A, the above throws an error
(x) `{ foo: 1, bar: 2 }`
( ) `{ foo: 1, 2: bar }`

?: Which of the following statements is _not true_ about this example?

```javascript
const obj = {
  outer: function() {
    const self1 = this

    const inner1 = () => {
      const self2 = this

      const inner2 = () => {
        const self3 = this
      }
    }
  }
}
```

( ) `self1 === self3`
( ) `self2 === self3`
( ) `self1 === self2`
(x) `self2 !== self3`

?: Which of the following statements is _not true_ about this example?

```javascript
const obj = {
  outer: function() {
    const self1 = this

    function inner1() {
      const self2 = this

      function inner2() {
        const self3 = this
      }
    }
  }
}
```

( ) `self1 !== self3`
( ) `self2 !== self3`
(x) `self1 === self2`
( ) `self2 !== self3`

?: What would be the constructor of `roger` in the example below?

```javascript
class Animal {
  constructor(noise) {
    this.noise = noise
  }

  speak() {
    console.log(this.noise)
  }
}

class Dog extends Animal {
  constructor(size) {
    super('bark!')

    this.size = size
  }
}

const roger = new Dog('large')
```

( ) `Animal`
(x) `Dog`
( ) `Object`
( ) `Function`

?: What is the result of the following?

```javascript
const speed = 'quick'

`The ${speed} brown fox jumps over the lazy dog.`
```

( ) `TypeError`
( ) `SyntaxError`
( ) 'The speed brown fox jumps over the lazy dog.'
(x) 'The quick brown fox jumps over the lazy dog.'

?: What is the value of `obj[123]` below?

```javascript
const obj = {
  [100 + 20 + 3]: 'party!'
}
```

( ) `undefined`
(x) `'party!'`

?: What is the final value of `array` below?

```javascript
const array = [1, 2, 3]
const extension = [4, 5, 6]

array = [...extension, ...array]
```

(x) `[1, 2, 3]`
( ) `[1, 2, 3, 4, 5, 6]`
( ) `[4, 5, 6, 1, 2, 3]`

???
