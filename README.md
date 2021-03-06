# Najlaa-big-o


# Big O Notation Exercises

### Part 1

Simplify the following big O expressions as much as possible:

1. `O(n + 10)`  => o(n)
2. `O(100 * n)` => o(n)
3. `O(25)`  => o(1)
4. `O(n^2 + n^3)` => o(n^3)
5. `O(n + n + n + n)` => o(n)
6. `O(1000 * log(n) + n)` => o(n)
7. `O(1000 * n * log(n) + n)` => o(n*log(n))
8. `O(2^n + n^2)` => o(2^n)
9. `O(5 + 3 + 1)` =>o(1)
10. `O(n + n^(1/2) + n^2 + n * log(n)^10)` => o(n*log(n))

### Part 2

Determine the time and space complexities for each of the following functions. If you're not sure what these functions do, copy and paste them into the console and experiment with different inputs!

```js
// 1.

function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
time =>  O(n)
space => O(1)

// 2.

function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}

time =>  O(1)
space => O(1)


// 3.

function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}

time =>  O(n)
space => O(1)



// 4.

function onlyElementsAtEvenIndex(array) {
  let newArray = Array(Math.ceil(array.length / 2));
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray[i / 2] = array[i];
    }
  }
  return newArray;
}
time =>  O(n)
space => O(n)
// 5.

function subtotals(array) {
  let subtotalArray = Array(array.length);
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray[i] = subtotal;
  }
  return subtotalArray;
}

time =>  O(n^2)
space => O(n)

```
