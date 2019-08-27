# Hard Core Functional Programming

In the beginning there was primordial soup

- Anything goes
- Everything changes
- Weird Names

```c
i = 0
i = i+1
PRINT i; " square = " i * i
IF i >= 10 THEN GOTO 60
GOTO 20
PRINT "Program Completed"
END
```

> Exercising restraint while coding feels weird at first, but it's worth it.

### Symptoms of GoTo Age
- Custom names
    - Naming is not good.
    ```js
    function daysThisMonth() {
        var date = new Date(),
        y = date.getFullYear(),
        m = date.getMonth(),
        start = new Date(y, m, 1),
        end = new Date(y, m+1, 1);
        return (end-start)/(1000*60*60*24);
    }
    
    function daysInMonth(y, m) {
        let start = new Date(y, m-1, 1),
            end = new Date(y, m, 1);
            return (end - start)/(1000*60*60*24);
- Looping patterns
- Glue Code
- Side Effects 


If you make your inputs explicit they are more easy to test. They are also more likely to run in other environment.

### How to Make your code Functional

- Seperate mutation from calculation    
    - Look for Mutations 

- Seperate functions from rules
    - Functions are nouns
> **Set Theoritically** Every function is a single-valued collection of pairs






```js
                   (-2, -1)
                    (0, 0)
    Left Side  --   (2, 1)  -- Right Side is called
    is Called       (4, 2)  Range of the function
    Domain          (8, 4)
    
```

- Seperate arity from functions
```js
    // Not Curried
    function get(property, object) {
        return object[property]
    }
    
    function getPersonName(person) {
        return get('name', person);
    }
    
    // Curried
    const get = property => object => object[property];
    
    const getName = get('name')
    const name = getName(person);
```
    
- Making your functions PURE make them
    - Testable
    - Portable
    - Memoizable
    - Parallelizable
