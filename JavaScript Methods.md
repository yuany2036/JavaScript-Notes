
# String Methods

<details>

<summary>Expand to see the String Methods</summary>

<br>

## **indexOf()**

<details>

<summary>This method returns the index position of the first instance of the specified substring.</summary>

<br>

> ### syntax
>> #### **indexOf(searchElement)** <br>
>> #### **indexOf(searchElement, fromIndex)**
> ### return value type:
>> **number**
> ### return value: 
>> **index value**
> ### mutating method:
>> **false**

<br>

```js
const string = "Hello World";
console.log(string.indexOf("e")); ➞ 1
```

<br>

The method would return `-1` if the specified value is no present within the string.

<br>

```js
const string = "Hello World";
console.log(string.indexOf("f")); ➞ -1
```

<br>

A second *optional* argument can be passed into the method to indicate at which index position the search should start at ***(inclusive)***. In the example below, there are three **Ls**, one at index position 2, index position 3, and position 9. So when 4 is given as the second argument, the search starts at index position 4, and returns the next **L** it encoutners, which is at index of 9.

<br>

```js
const string = "Hello World";
console.log(string.indexOf("l", 4)); ➞ 9
```
</details>

<br>

## **lastIndexOf()**

<details>

<summary>This method returns the index position of the last instance of the specified substring.</summary>

<br>

> ### syntax
>> #### **lastIndexOf(searchElement)** <br>
>> #### **lastIndexOf(searchElement, fromIndex)**
> ### return value type:
>> **number**
> ### return value: 
>> **index value**
> ### mutating method:
>> **false**

<br>

> The method does the same as indexOf, but starts the search at the back of the string, and searches ***forwards***.

<br>

```js
const string = "Hello World";
console.log(string.indexOf("l")); ➞ 9
```

The method would return `-1` if the specified value is no present within the string.

```js
const string = "Hello World";
console.log(string.indexOf("f")); ➞ -1
```

A second *optional* argument can be passed into the method to indicate at which index position the search should start at ***(inclusive)***. In the example below, there are three `l`s, one at index position **2**, index position **3**, and position **9**. So when **4** is given as the second argument, the search starts at index position **4**, and returns the next `l` it encounters, which is at index of **3**.

```js
const string = "Hello World";
console.log(string.indexOf("l", 4)); ➞ 3
```
</details>

<br>

## **includes()**

<details>

<summary>This method performs a search through the string whether or not a substring is present within it.</summary>

<br>

> ### syntax:
>> **includes(searchString)** <br>
>> **includes(searchString, position)**
> ### return value type:
>> **boolean**
> ### mutating method:
>> **false**

<br>

An important thing to note is that the search `includes()` performs is ***case-sensitive***, so it might be prudent to change the string to an all uppercase or all lowercase string before using `includes()`.

<br>

```js
const string = "Hello World";
console.log(string.includes("Hello")); ➞ true
console.log(string.includes("hello")); ➞ false
```

<br>

An *optional* second argument can be passed through to indicate at which index position the search should begin; if no such argument is provided, it would default to 0.

<br>

```js
const string = "Hello World";
console.log(string.includes("H", 1)); ➞ false
```
</details>

<br>

## **slice()**

<details>

<summary>This method allows you to create a new string from a user-defined section of a string</summary>

<br>

> ### syntax:
>> **slice()** <br>
>> **slice(indexStart)** <br>
>> **slice(indexStart, indexEnd)**
> ### return value type:
>> **string**
> ### mutating method:
>> **false**

<br>

The method takes two arguments: the first one indicates at which index position the slicing should start *inclusively*, and the second one where it should end *exclusively*.

<br>

If no second argument is provided, the returned string would be a substring that starts from the index start and includes all characters until the end of the string.

<br>

**Example with no second argument:**

```js
const string = "0123456789";
console.log(string.slice(4)); ➞ "456789"
```

<br>

**Example with second argument:**

```js
const string = "0123456789";
console.log(string.slice(4, 8)); ➞ "4567"
```

<br>

If the argument provided is a negative value, the position is counted from the end of the string.

<br>

**Example with a negative value as an argument**

```js
const string = "0123456789";
console.log(string.slice(-0)); ➞ "0123456789"
```

```js
const string = "0123456789";
console.log(string.slice(-4)); ➞ "6789"
```

> Keep in mind that even when a negative value is provided, the process is still going from left to right, hence the `indexEnd` would still have to be greater than `indexStart`.

```js
const string = "0123456789";
console.log(string.slice(-4, -1)); ➞ "678"
```

</details>

<br>

## **toUpperCase()**

<details>

<summary>This method returns the calling string value converted to uppercase (the value will be converted to a string if it isn't one).</summary>

<br>

> ### syntax:
>> **toUpperCase()**
> ### return value:
>> **string**
> ### mutating method:
>> **false**

<br>

**Example of toUpperCase()**

```js
const string = "all lower cases";
console.log(toUpperCase(string)); ➞ "ALL LOWER CASES"
```

</details>

<br>

## **toLowerCase()**

<details>

<summary>This method returns the calling string value converted to lowercase (the value will be converted to a string if it isn't one).</summary>

<br>

> ### syntax:
>> **toLowerCase()**
> ### return value:
>> **string**
> ### mutating method:
>> **false**

<br>

**Example of toLowerCase()**

```js
const string = "ALL UPPER CASES";
console.log(toLowerCase(string)); ➞ "all upper cases"
```

</details>

<br>

## **trim()**

<details>

<summary>This method removes any white spaces that comes before the first character in the string and any that comes after the last character.</summary>

<br>

> ### syntax:
>> **trim()** <br>
>> **trimStart()** <br>
>> **trimEnd()**
> ### return value:
>> **string**
> ### mutating method:
>> **false**

<br>

This method doesn't take any arguments, and has two different variations to it: `trimStart()` and `trimEnd()`.

<br>

**Example of using trim**
```js
const string = "	Hello World		";
console.log(string.trim()); ➞ "Hello World"
```

<br>

**Example of using trimStart**
```js
const string = "	Hello World		";
console.log(string.trimStart()); ➞ "	Hello World"
```

<br>

**Example of using trimEnd**
```js
const string = "	Hello World		";
console.log(string.trimEnd()); ➞ "		Hello World"
```

</details>

<br>

## **charAt()**

<details>

<summary>This method returns a single character of a string at the specified index position.</summary>

<br>

> ### syntax:
>> **charAt(index)**
> ### return value type:
>> **string**
> ### mutating method:
>> **false**

<br>

Since strings can be thought of as *an array of characters*, you can access the individual characters by using the index number.

<br>

**Example of using charAt:**

```js
const string = "0123456789";
console.log(string.charAt(4)); ➞ "4"
const string2 = "Hello World";
console.log(string2.charAt(6)) ➞ "W";
```

</details>

<br>

## **charCodeAt()**

<details>

<summary>This method returns the UTF-8 code for the character at the specified index position.</summary>

<br>

> ### syntax:
>> **charCodeAt(index)**
> ### return value type:
>> **number**
> ### mutating method:
>> **false**

<br>

**Examples of using charCodeAt()**

```js
const string = "Lily";
console.log(string.charCodeAt(0)); ➞ 76
```

<br>

> Notice that when using `charCodeAt()` on a character that is of a different case(lower case or upper case), the number that is returned would be different.

<br>

```js
const string = "Lily";
console.log(string.charCodeAt(2)); ➞ 108
```

<br>

**See below for a chart of ASCII, which is a subset of UTF-8, but already contains most of the common characters used on a daily basis:**

![alt text](images/Screenshot%20from%202022-09-29%2016-41-51.png)


<br>

</details>

<br>

## **split()**

<details>

<summary>This method takes a string and returns it as an array.</summary>

<br>

> ### syntax:
>> **split()** <br>
>> **split(separator)** <br>
>> **split(separator, limit)**
> ### return value type:
>> **array**
> ### mutating method:
>> **false**

<br>

The method takes a string, and splits it (or takes the entire string if no separator is provided) into an array. The string is split by all matches to the separator **without** including the separator in the result.

<br>

Up to two arguments can be provided, but both are optional. The first argument is the `separator` argument, and this determines at which points the string is split into elements for the array.

<br>

**Example of `split()` without a separator:**

```js
const string = "We are survival machines";
console.log(string.split()); ➞ ["We are survival machines"]
```

<br>

**Example of `split()` with a white space as the separator, splitting the string by words:**

```js
const string = "We are survival machines";
console.log(string.split(" ")); ➞ ["We", "are", "survival", "machines"]
```

<br>

The second argument, the `limit`, determines how many elements are put into the array. Once the limit has been reached, all remaining elements are discarded.

<br>

**Example of `split()` with a `limit` argument:**

```js
const string = "We are survival machines";
console.log(string.split(" ", 2)); ➞ ["We", "are"]
```

</details>

<br>

</details>

<br>

# Array Methods

<details>

<summary>Expand to see the Array Methods</summary>

## **pop()**

<details>

<summary>This method extracts the last item inside an array and returns it.</summary>

<br>

> ### syntax:
>> **pop()**
> ### return value type:
>> **N/A**
> ### return value:
>> **last element of target array**
> ### mutating method:
>> **true**

<br>

The `pop()` method is a mutating method. It changes the contents and length of the target array. If you wish to extract the last element array without mutating it, consider using `slice()` instead. 

<br>

If `pop()` is used on an empty array, `undefined` will be returned.

<br>

> the `shift()` methods works in a similar way, but applies its effect to the **first** element of an array instead of the last.

**Example of the pop() method:**

```js
const movies = ["The Dark Knight", "Crouching Dragon, Hidden Tiger", "Mud"];
console.log(movies.pop()); ➞ "Mud"
```

</details>

<br>

## **push()**

<details>

<summary>This method adds one or more elements to the end of an array and returns the new length of the array.</summary>

<br>

> ### syntax:
>> **push(element0)** <br>
>> **push(element0, element1)** <br>
>> **push(element 0, element1, ..., elementN)**
> ### return value type:
>> **number**
> ### return value:
>> **new length of array**
> ### mutating method:
>> **true**

<br>

The `push()` method is a mutating method. It changes the contents and length of the target array.

<br>

> the `unshift()` methods works in a similar way, but applies its effect to the **beginning** of an array instead of the end.

<br>

**Example of the `push()` method:**

```js
const movies = ["The Dark Knight", "Crouching Dragon, Hidden Tiger", "Mud"];
console.log(movies.push("Dune")); ➞ 4
```

</details>

<br>

## **shift()**

<details>

<summary>This method extracts the first item inside an array and returns it.</summary>

<br>

> ### syntax:
>> **shift()**
> ### return value type:
>> **N/A**
> ### return value:
>> **first element of target array**
> ### mutating method:
>> **true**

<br>

The `shift()` method is a mutating method. It changes the contents and length of the target array. If you wish to extract the first element array without mutating it, consider using `slice()` instead.

<br>

If `shift()` is used on an empty array, `undefined` will be returned.

<br>

> the `pop()` methods works in a similar way, but applies its effect to the **last** element of an array instead of the first.

<br>

**Example of the shift() method:**

```js
const movies = ["The Dark Knight", "Crouching Dragon, Hidden Tiger", "Mud"];
console.log(movies.shift()); ➞ "The Dark Knight"
```

</details>

<br>

## **unshift()**

<details>

<summary>This method adds one or more elements to the start of an array and returns the new length of the array.</summary>

<br>

> ### syntax:
>> **unshift(element0)** <br>
>> **unshift(element0, element1)** <br>
>> **unshift(element 0, element1, ..., elementN)**
> ### return value type:
>> **number**
> ### return value:
>> **new length of array**
> ### mutating method:
>> **true**

<br>

The `unshift()` method is a mutating method. It changes the contents and length of the target array.

<br>

> the `push()` methods works in a similar way, but applies its effect to the **end** of an array instead of the beginning.

<br>

**Example of the `unshift()` method:**

```js
const movies = ["The Dark Knight", "Crouching Dragon, Hidden Tiger", "Mud"];
console.log(movies.unshift("Dune")); ➞ ["Dune", "The Dark Knight", "Crouching Dragon, Hidden Tiger", "Mud"]
```

</details>

<br>

## **splice()**

<details>

<summary>This method changes the contents and length of an array by removing or replace existing elements and/or adding new elements.</summary>

<br>

> ### syntax:
>> **splice(start)** <br>
>> **splice(start, deleCount)** <br>
>> **splice(start, deleCount, item1)** <br>
>> **splice(start, deleCount, item1, item2, itemN)**
> ### return value type:
>> **array**
> ### return value:
>> **array containing deleted elements**
> ### mutating method:
>> **true**

<br>

If only one single argument is provided, it would be taken as the argument `start`, and used to indicate where the ***splicing*** would begin. All elements that are after located at index positions after `start` would then be removed from the original array and returned as a new array.

<br>

**Example of using one single argument with `splice()`:**

```js
const numbers = [0, 1, 2, 3, 4, 5, 6];
console.log(numbers.splice(3)); ➞ [3, 4, 5, 6] // This is the returned array
console.log(numbers); ➞ [0, 1, 2] // The original array
```

<br>

When a second argument is provided, it would then become the ***number of elements to be removed***. All the elements between the start and end would be removed and returned as a new array, while the rest remain inside the original array.

<br>

**Example of using two arguments with `splice()`:**

```js
const numbers = [0, 1, 2, 3, 4, 5, 6];
console.log(numbers.splice(3, 2)); ➞ [3, 4] // This is the returned array
console.log(numbers); ➞ [0, 1, 2, 5, 6] // The original array
```

<br>

When a third argument is provided, it would then be whatever it is that needs to be inserted into the array at the indicated position (`start`). If you only wish to insert elements into an array without removing any, you can provide `0` as the second argument, in which case no element would be removed.

<br>

**Example of using three or more arguments with `splice()`, while *not* removing any elements:**

```js
const numbers = [0, 1, 2, 4, 5, 6];
console.log(numbers.splice(3, 0, 3)); ➞ [] // An empty array is returned, as no elements are removed
console.log(numbers); ➞ [0, 1, 2, 3, 4, 5, 6] // The original array
```
<br>

**Example of using three or more arguments with `splice()`, removing and replacing elements:**

```js
const numbers = [0, 1, 2, 8, 9, 5, 6];
console.log(numbers.splice(3, 2, 3, 4)); ➞ [8, 9] // // Returned array with removed elements
console.log(numbers); ➞ [0, 1, 2, 3, 4, 5, 6] // The original array
```

</details>

<br>

## **slice()**

<details>

<summary>This method copies a target array either in its entirety or a portion of it</summary>

<br>

> ### syntax:
>> **slice()** <br>
>> **slice(start)** <br>
>> **slice(start, end)**
> ### return value type:
>> **array**
> ### mutating method:
>> **false**

<br>

The `slice()` method creates a copy of an array, and depending on the arguments given, either copies the entire target array or just a portion or it. When no arguments are provided, the entire array is copied and returned.

<br>

**Example of using no arguments with the `slice()` method:**

```js
const array = [0, 1, 2, 3];
console.log(array.slice()); ➞ [0, 1, 2, 3]
```

<br>

If a single argument is given, it will be taken as the `start` argument. This indicateds at which ***index position*** the copying should begin (*inclusively*), and will copy everything that comes after it.

<br>

**Example of using a `start` argument with the `slice()` method:**

```js
const array = [0, 1, 2, 3];
console.log(array.slice(1)); ➞ [1, 2, 3]
```

<br>

If a second argument is given, it will be taken as the `end` argument, and it will indicated at which ***index position*** the copying should end (*exclusively*). 

<br>

**Example of using a `start` and an `end` argument with the `slice()` method:**

```js
const array = [0, 1, 2, 3];
console.log(array.slice(1, 3)); ➞ [1, 2] // 3 being at index position 3 is excluded
```

</details>

<br>

## **concat()**

<details>

<summary>This method is used to combine two or more arrays into one.</summary>

<br>

> ### syntax:
>> **concat()** <br>
>> **concat(value0)** <br>
>> **concat(value0, value1)** <br>
>> **concat(value0, value1, /* … ,*/ valueN)**
> ### return value type:
>> **array**
> ### return value:
>> **combined array**
> ### mutating method:
>> **false**

<br>

When using the `concat()` method without any arguments, you will simply be returned a copy of the array in its entirety.

<br>

**Example of using `concat()` with no arguments:**

```js
const array = [0, 1, 2, 3];
console.log(array.concat()); ➞ [0, 1, 2, 3]
```

<br>

When one or more values are provided, these would then become the elements that will be combined with the target array and returned to you, leaving the target array unchanged.

<br>

**Example of using `concat()` with arguments:**

```js
const array = [0, 1, 2, 3];
console.log(array.concat(4, 5)); ➞ [0, 1, 2, 3, 4, 5]
console.log(array) ➞ [0, 1, 2, 3] // The target array remains unchanged
```

**Example of combining two arrays with `concat()`:**

```js
const letters = ["a", "b", "c"];
const numbers = [1, 2, 3];

const alphaNumeric = letters.concat(numbers);
console.log(alphaNumeric); ➞ ['a', 'b', 'c', 1, 2, 3]
```

<br>

**Example of combining three arrays with `concat()`:**

```js
const num1 = [1, 2, 3];
const num2 = [4, 5, 6];
const num3 = [7, 8, 9];

const numbers = num1.concat(num2, num3);

console.log(numbers); ➞ [1, 2, 3, 4, 5, 6, 7, 8, 9]
```

</details>

<br>

## **reverse()**

<details>

<summary>This method reverses the order of any given array.</summary>

<br>

> ### syntax:
>> **reverse()**
> ### return value type:
>> **array**
> ### return value:
>> **reversed array**
> ### mutating method:
>> **true**

<br>

The `reverse()` method takes any given array, and reverses the order of the elements in the array. The original array is modified, and returned, ***no copy is made using this method***.

<br>

**Example of using `reverse()`:

```js
const array = [0, 1, 2, 3];
console.log(array.reverse()); ➞ [3, 2, 1, 0]

console.log(array); ➞ [3, 2, 1, 0] // The original array is modified as well
```

<br>

</details>

<br>

## **indexOf()**

<details>

<summary>This method searches through an array, and returns index position of the first instance of a matching elements</summary>

<br>

> ### syntax:
>> **indexOf(searchElement)** <br>
>> **indexOf(searchElement, fromIndex)**
> ### return value type:
>> **number**
> ### return value:
>> **index or -1 for non-existing elements**
> ### mutating method:
>> **false**

<br>

The `indexOf()` method requires at least one argument, the `searchElement` argument: what is it that you want to search for within the array?

<br>

Using `indexOf()` would always return the index position of the first instance of a match. In the example below, the second 2's position (index position 3) isn't presented, because there was a previous match.

<br>

**Example of using `indexOf()` with just one argument:**

```js
const array = [2, 9, 8, 2];
array.indexOf(2); ➞ 0
array.indexOf(7); ➞ -1 
```
> When the searched element isn't present within the array, `-1` is returned.

<br>

An optional second argument can be given, which would be the `fromIndex` argument: where within the array should the search begin?
This can be useful for when you want to find the index position of all instances of a certain `searchElement`. If there are multiple `a`s inside an array, and you want to find the position for all of them, the example below can be helpful.

<br>

**Example of using a `While Loop` combined with `indexOf()`:**

```js
const indices = [];
const array = ['a', 'b', 'a', 'c', 'a', 'd'];
const element = 'a';
let idx = array.indexOf(element);
while (idx !== -1) {
  indices.push(idx);
  idx = array.indexOf(element, idx + 1);
}
console.log(indices); ➞ [0, 2, 4]
```

</details>

<br>

## **join()**

<details>

<summary>This method creates and returns a new string by concatenating all of the elements in an array, separated by commas or a specified separator string.</summary>

<br>

> ### syntax:
>> **join()** <br>
>> **join(separator)**
> ### return value type:
>> **string**
> ### return value:
>> **elements from an array concatenated into a string**
> ### mutating method:
>> **false**

<br>

The `separator` specifies a string to separate each pair of adjacent elements of the array.
> - If omitted, the array elements are separated with a comma (","). 
> - If separator is an empty string, all elements are joined without any characters in between them.

<br>

```js
const a = ['Wind', 'Water', 'Fire'];
a.join();       ➞ 'Wind,Water,Fire'
a.join(', ');   ➞ 'Wind, Water, Fire'
a.join(' + ');  ➞ 'Wind + Water + Fire'
a.join('');     ➞ 'WindWaterFire'
```

</details>

<br>

## **includes()**

<details>

<summary>This method determines whether an array includes a certain value among its entries, returning true or false as appropriate.</summary>

<br>

> ### syntax:
>> **includes(searchElement)** <br>
>> **includes(searchElement, fromIndex)**
> ### return value type:
>> **boolean**
> ### mutating method:
>> **false**

<br>

The `includes()` method requires at least one argument, the `searchElement` argument: what is it that you want to search for within the array?

<br>

**Examples of using `includes()` with one argument:**

```js
[1, 2, 3].includes(2)         ➞ true
[1, 2, 3].includes(4)         ➞ false
[1, 2, NaN].includes(NaN)     ➞ true
["1", "2", "3"].includes(3)   ➞ false
```

<br>

An optional second argument can be given, which would be the `fromIndex` argument: where within the array should the search begin?

<br>

**Examples of using `includes()` with a second argument:**

```js
[1, 2, 3].includes(3, 3)  ➞ false
[1, 2, 3].includes(3, -1) ➞ true
```

<br>

> If `fromIndex` is greater than or equal to the length of the array, false is returned. The array will not be searched.

</details>

<br>

## **sort()**

<details>

<summary>This method sorts the elements of an array and returns the same array, now sorted.</summary>

<br>


> ### syntax:
>> **sort() ➞ Functionless** <br>
>> **sort((a, b) => { } ) ➞ Arrow function** <br>
>> **sort(compareFn) ➞ Compare function** <br>
>> **sort(function compareFn(a, b) { }) ➞ Inline compare function**
> ### return value type:
>> **array**
> ### return value:
>> **sorted array**
> ### mutating method:
>> **true**

<br>

The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values. When using the `sort()` method without using a function, then the array will be sorted in lexicographical order.

<br>

**Example of `sort()` using no function:**

```js
const array = [65, 78, 9, 11, 2, 0, 12];
array.sort();
console.log(array); ➞ [0, 11, 12, 2, 65, 78,  9] // Because it is sorted lexicographically, numbers don't sort quite the way we want
```

<br>

To sort an array of numbers, we'll have to add a function to it to define how the array should be sorted.

<br>

**The table below outlines how any two numbers will be sorted in relation to each other depending on the outcome of the function.**

<br>

| compareFn(a, b) return value | sort order                     |
|------------------------------|--------------------------------|
| > 0                          | sort a after b                 |
| < 0                          | sort a before b                |
| === 0                        | keep original order of a and b |

> For example, if `a - b` is greater than 0, then `a` would be placed behind `b`.

<br>

**Example of the `sort()` method with an arrow function, sorting in ascending order:**

```js
const array = [65, 78, 9, 11, 2, 0, 12];
array.sort((a, b) => a - b);
console.log(array); ➞ [0,  2,  9, 11, 12, 65, 78]
```

<br>

**Example of the `sort()` method with an arrow function, sorting in descending order:**

```js
const array = [65, 78, 9, 11, 2, 0, 12];
array.sort((a, b) => b - a);
console.log(array); ➞ [78, 65, 12, 11, 9,  2,  0]
```

</details>

<br>

## **toString()**


<details>

<summary>This method takes an array, and converts it into a string, combining the different elements using the join method.</summary>

<br>

> ### syntax:
>> **toString()**
> ### return value type:
>> **string**
> ### mutating method:
>> **false**

<br>

**Example of using the `toString()` method:**

```js
const array1 = [1, 2, 'a', '1a'];
console.log(array1.toString()); ➞ "1,2,a,1a"
```

</details>

</details>