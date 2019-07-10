# Js-Module1-Problems
Javascript Problems 



/* Write a function called "getElementsGreaterThan10AtProperty".

Given an object and a key, "getElementsGreaterThan10AtProperty" returns an array containing the elements within the array, located at the given key, that are greater than 10.

Notes:

create new var = []
for loop to iterate over object and create new var

If the array is empty, it should return an empty array.
If the array contains no elements greater than 10, it should return an empty array.
If the property at the given key is not an array, it should return an empty array.
If there is no property at the key, it should return an empty array.
var obj = {
  key: [1, 20, 30]
};
var output = getElementsGreaterThan10AtProperty(obj, 'key');
console.log(output); // --> [20, 30]
*/

/* My Pseudo Code
1. create an empty array
2. use for...in loop to iterate over the property values
3. use a conditional to select the numbers that are over 10
4. the obj[key][nums] is being pushed inside the emptyArr
5. return it
*/

function getElementsGreaterThan10AtProperty(obj, key) {
    // your code here
    var emptyArr = []; // (1)

    for(var nums in obj[key]) { // (2)
        if(obj[key][nums] > 10) { // (3)
            emptyArr.push(obj[key][nums]); // (4)
        }
    }
    return emptyArr; // (5)
  }

var obj = {
    key: [1, 20, 30]
  };
  var output = getElementsGreaterThan10AtProperty(obj, 'key');
  console.log(output); // --> [20, 30]




/* Write a function called "getFirstElementOfProperty".

Given an object and a key, "getFirstElementOfProperty" returns the first element of the array located at the given key.

Notes:

If the array is empty, it should return undefined.
If the property at the given key is not an array, it should return undefined.
If there is no property at the key, it should return undefined.
var obj = {
  key: [1, 2, 4]
};
var output = getFirstElementOfProperty(obj, 'key');
console.log(output); // --> 1
*/

/* Pseudo Code
1. conditional that states !Array.isArray ((method) ArrayConstructor.isArray(arg: any): arg is any [] - so 'obj' and 'key' is passed in here ALSO - - the instructions say : "If the property at the given key is not an array, it should return undefined."
2. return undefined 
3. else, return object key at index 0
*/

/* My Solution */
function getFirstElementOfProperty(obj, key) {
    // your code here
    if(!Array.isArray(obj[key])) { // (1)
        return undefined; // (2)
    } else {
        return obj[key][0]; // (3)
    }
  }

var obj = {
    key: [1, 2, 4]
  };
  var output = getFirstElementOfProperty(obj, 'key');
  console.log(output); // --> 1




/* Write a function called "getNthElementOfProperty".

Given an object and a key, "getNthElementOfProperty" returns the nth element of an array located at the given key.

Notes:

If the array is empty, it should return undefined.
If n is out of range, it should return undefined.
If the property at the given key is not an array, it should return undefined.
If there is no property at the key, it should return undefined.
var obj = {
  key: [1, 2, 6]
};
var output = getNthElementOfProperty(obj, 'key', 1);
console.log(output); // --> 2
*/

/* My Pseudo Code 
1. if not an array, isArray takes in obj and [key] {}
2. returns undefined
3. else returns obj key and [n] which is the number
*/

/* My Solution */
function getNthElementOfProperty(obj, key, n) {
    // your code here
    if(!Array.isArray(obj[key])) {
        return undefined;
    } else {
        return obj[key][n];
    }
  }

var obj = {
    key: [1, 2, 6]
  };
  var output = getNthElementOfProperty(obj, 'key', 1);
  console.log(output); // --> 2





/*Write a function called "getLastElementOfProperty".

Given an object and a key, "getLastElementOfProperty" returns the last element of an array located at the given key.

Notes:

If the array is empty, it should return undefined.
if the property at the given key is not an array, it should return undefined.
If there is no property at the key, it should return undefined.
var obj = {
  key: [1, 2, 5]
};
var output = getLastElementOfProperty(obj, 'key');
console.log(output); // --> 5
 */

   /* My Pseudo Code 
 1. create new var and set it equal to the obj key.length -1 so that it can access the last element each time
 2. return obj[key][lastElem];
 */

 /* My Solution */
function getLastElementOfProperty(obj, key) {
    // your code here
    if(!Array.isArray(obj[key])) {
        return undefined;
    } else {
        var lastElem = obj[key].length - 1;
        return obj[key][lastElem];
    }
  }

var obj = {
    key: [1, 2, 5]
  };
  var output = getLastElementOfProperty(obj, 'key'); // must define location inside function
  console.log(output); // --> 5

