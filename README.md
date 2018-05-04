# JavaScript: The Good Parts 
##### By Douglas Crockford 

### Chapter 8: Methods

In this chapter the author goes over some of the common methods on standard JavaScript data types. Here I'll go over some of the methods I find most useful, as well as methods that I wasn't aware of before reading this chapter. As in the book, they are grouped by type. 

##### Array Methods

> array.concat(item...)

This method produces a copy of the array that it's called on with the arguments appended to it. If you pass it an array, it will append the elements of the array.

> array.reverse()

Reverses the order of the elements in the array.
```
var arr = [ 'a', 'b', 'c'];
arr.reverse();
console.log(arr); 
// => ['c', 'b', 'a']
```

> array.shift()

Basically the opposite of `array.pop()` . Removes the first element in the array and returns it.

>array.slice(start, end)

Makes a new array out of a portion of the array that it was called on. The `start` parameter will be the first element in the array, and the `end` parameter is not included in the new array. This is why instead of `end`, I prefer to think of the second parameter as `length`. If this parameter is not given, the default is `array.length`. 

>array.sort(compareFn)

Sorts the contents of an array in place. The optional `compareFn` argument can be used to sort numbers. Without this argument, the array will be sorted based on the Unicode point value of each item. On an array of numbers, it will convert each number to a string to get the Unicode point value.

>array.splice(start, deleteCount, item...)

Splice removes elements in the array and replaces them with new ones.  The `start` parameter is the index of the first item to be removed, and the `deleteCount` is how many items should be removed.

##### Number Methods
>number.toPrecision(precision)

Converts the number to a string in the decimal form. The `precision` parameter controls the number of digits of precision. 

```
console.log(Math.PI.toPrecision(4));
//=> 3.141
```
##### Object Methods
>object.hasOwnProperty(name)

Returns a boolean to reflect whether or not the object contains a property matching the `name` parameter. 
##### String Methods
>string.charAt(pos)

Returns the character of the string at the position of the `pos` parameter.

>string.concat(string...)

Creates a new string by concatenating the string(s) passed in as the `string...` argument to the original string.

>string.indexOf(searchString, position)

Searches for the `searchString` within the strin. If it finds it, it returns the position of the first matched character. If not, it returns `-1`. 

>string.replace(searchValue, replaceValue)

Searches the string for the `searchValue`, and if it finds it, returns a new string with the `searchValue` replaced with the `replaceValue`.

>string.slice(start, end)

Does a very similar operation to `array.slice()` but with a string.

>string.split(separator, limit)

Creates an array of strings by splitting this string into pieces, based on the `separator` parameter.

>string.substring(start, end) 

Same as `slice()` but doesn't handle negative parameters. According to the book, there isn't a reason to use `substring`.


