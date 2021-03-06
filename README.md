# Clear-Expressions
converts JSON  into Mathematical expression,Simplifies it and solve it.


# Description
You will be given a JSON file as an input. This file will contain a equation in a structured format
like this:
```
{
"op": "equal",
"lhs": {
"op": "add",
"lhs": 1,
"rhs": {
"op": "multiply",
"lhs": "x",
"rhs": 10
}
},
"rhs": 21
}
```
This particular example represents this equation:
1 + (x * 10) = 21

# Features

* Parses the JSON into a structured format, and pretty-prints the parsed
  equation, in a single line with brackets, like the below example.
  ```
  1 + (x * 10) = 21
  ```
* Transforms the expression so that you have ‘x’ on one side, and all the operations on the
  other side. In this example, a transformed expression can be:
  ```
  x = (21 − 1) / 10
  ```
* Evaluates the expression on the other side and finds the value of ‘x’.
  For our input files, assume that ‘x’ is always solvable.
  ```
  x = 2
  ```

# Notes:
* The operations possible are: add, subtract, multiply, divide, and equal
* Each operation will have a LHS and a RHS. The LHS / RHS of a operation can be:
  1. another operation,
  2. Or a fixed number,
  3. Or a variable reference
* The input files will be limited to have the following characteristics:
  1. Top level operation will always be ‘equal’
  2. RHS will always be a fixed number
  3. LHS can be complex. But there will only be a single variable reference (x) that
     occurs somewhere in the LHS. All other leaf nodes will be fixed numbers.
     
# Usage

Run the following commands :

```
$ npm install
```
then

```
$ node main.js
```
# Requirements

- Node.js

# Help & Support
<ul>
  <li><a href="https://in.linkedin.com/in/itsksaurabh">Author</a></li>
</ul>
