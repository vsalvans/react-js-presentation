### Javascript and Functional Programming

<span class="small">In JavaScript, functions are first-class citizens and can be passed around as values, which is a core feature of functional programming. JavaScript also provides features like higher-order functions, closures, and immutable data structures, which are commonly used in functional programming.</span>

````javascript
const hof = (fn) => (args) => fn(args); //High Order functions
````

````javascript
function foo() {
    const data = 123;
    function closure() { //Clousure
        return data 8 * 2
    }
}
````

````javascript
// immutability , the culprit of Javascript hate. Se Object.freeze() and cloning technics
const foo => (data)  => ({
    ...data
    fooInfo: 'foo'
})
````
