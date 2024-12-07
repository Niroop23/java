````**script tag is to be written after the body tag.
This is so because the browsers work from top to bottom , also js takes in elements from the body to maipulate if we were to guve script before body the js wil not be able to identify tyhe element therefore giving an eroor.
So we write script tag after body tag so that the browser can first load the body and then the js can manipulate the elements of the body.**

array methods:-

push([ele]):it is used to ad an element/another array at the end of the array.

pop():it is used to remove the last element of the array.

shift():it is used to remove the first element of the array.

unshift([ele]):it is used to add an element/another array at the beginning of the array.

---

functions:

function sampleFunc(parameters) {
some code;
}

sampleFunc(arguement)

#by default return value if not defined is undefined.

scopes:
global scope: variables declared outside of any function are in global scope.
local scope: variables declared inside a function are in local scope.

-> typeof keyword id used to find the type of the variable.

-> if we declare a variable inside a function without using the keyword var it is considered as a global variable.

-> if we declare two variable with the same name, one globally and the other locally .if we display the variable the outer variable is shown.
but if we print inside the func itself then the local variabe takes precedence over global variable.

---

Equality(==) vs strict Equality(===)

equality converts both the operand into same data type for comparision where as
strict equality checks for both value and data type.

inequality(!=) vs strict inequality(!==)

inequality checks if both the values are not equal where as
strict inequality checks if both the values and data types are not equal.

---

In JS objects can be declared by following notation
var obj = {
attritube1,
attribute2,
...so on(properties of the object)

};

these props can be of any data type;
and can be accessed using
1.dot notation(obj.attribute1)
2.bracket notation(obj['attribute1'])

the second is use full if the property inside the object has a space in its name
like obj{
"attribute 1":"abc"

};

==>Accessing object properties with variables

for example;

JavaScript
var obj = {
    1:"abc",
    2:"ghi",
    3:"jkl"
};


var playernumb=2;
var player=obj[player numb];

if we console.log(player)
it will print "ghi"..

==>Updating object properties

obj.attribute1="new value";

in the above example
we can update the value of 2 by

obj[2]="new value";


==>adding new properties to an existng object

This can be done using both notations:

1.obj.newAttribute="new value";

2.obj['newAttribute']="new value";


==>Delete properties from an object

1.delete obj.attribute1;

2.delete obj['attribute1'];

--------------

We can use objects for look ups instead of using switch statements like following

function lookup(val){

    var result="";

    switch(val)
    {
        case "a":
            result="alpha";
            break;

        case "b":
            result="beta";
            break;

        case "c":
            result="gamma";
            break;

        default:
        result="not found";

    }
}

instead of the switch statements we can use the concept of objects
like following

function lookup(val){
    var look ={
        "a":"alpha",
        "b":"beta",
        "c":"gamma"

        };
    res= look[val];
    return res || "not found";
}

==>Testing objects for properties
1.in operator
if("attribute1" in obj){
    console.log("obj has attribute1");
    }
else
{
    console.log("obj does not have attribute1");
    }

2.hasOwnProperty() method
if(obj.hasOwnProperty("attribute1")){
    console.log("obj has attribute1");
    }
else
{
    console.log("obj does not have attribute1");
    }


3.Object.keys() method
var keys = Object.keys(obj);
if(keys.indexOf("attribute1")>-1){
    console.log("obj has attribute1");
    }
else
{
    console.log("obj does not have attribute1");
    }

==>Manipulating complex objects

we can create an array with multiple objects in it seperated by comma","
like following


var people = [

    {name: "John",
     age:  (new Date()).getFullYear() - 1990
    },

    {name: "Jane",
    age: (new Date()).getFullYear() - 1995}

];
    We can access the objects in the array using their index like `people[0].name` or
    `people[1].age`

    We can also use for loop to iterate over the array of objects like following

    for(var i = 0; i < people.length; i++){
        console.log(people[i].name + " is " + people[i].age + " years)
        }


==>Nested objects
We can create nested objects like following
var storage={
    "car": {
        "inside":
        {
            "glove box":"maps",
            "passenger seat":"crumbs"
        }

        "outside":
        {
            "trunk":"jack"
        }

    },

};
We can access the nested objects like following
storage.car.inside["glove box"] or storage.car.outside.trunk


==>nested arrays
We can create nested arrays like following

var myPlants =[
    {
        type: "flowers",
    list: [
        "rose",
        "tulip",
        "daisy"

        ]
    },

    {
        type:"trees",
    list: [
        "oak",
        "pine",
        "maple"
        ]
    }

];

We can access the nested arrays like following
myPlants[0].list[0] or myPlants[1].list[1]

--------------------------------------------

generate random fractions
Math.random() returns a random number between   0 (inclusive) and 1 (exclusive).

generating random whole numbers
Math.floor(Math.random() * 10) returns a random whole number between 0 and 9.[inclusiv  e both]


parseint function
The parseInt() function parses a string and returns an integer. If the string does not contain a number
it returns NaN (Not a Number).

radix
The radix parameter is used to specify the base of the number in the string. For example, if
the radix is 16, the function will parse the string as a hexadecimal number.

default is base 10.
------------------------------------------

Ternary operator
The ternary operator is a shorthand way of writing an if-else statement. It takes three arguments
condition ? trueValue : falseValue
------------------------------------------


Multiple ternary operator
var age = 18;
var message = (age >= 18) ? "You are eligible to vote" : (age  >= 16) ? "You are eligible to drive" : "You are not eligible to vote

or drive";
------------------------------------------

var keyword vs let keyword

var keyword is function scoped whereas let keyword is block scoped.
------------------------------------------
"use strict" keyword

The "use strict" keyword is used to enable strict mode in JavaScript. In strict mode, JavaScript
shows more errors and exceptions, and it does not allow some actions that are allowed in
non-strict mode.
------------------------------------------

Const keyword

The const keyword is used to declare a constant. A constant is a variable that cannot be
changed once it is declared. Constants are block-scoped, much like variables declared using the let keyword
------------------------------------------

Mutating an array declared with const

Although the array itself cannot be reassigned, its elements can be changed. This is because
the const keyword only prevents the reassignment of the variable, not the mutation of its
value.using bracket notation.
------------------------------------------


==>preventing object mutation
Object.freeze("object name") method can be used to prevent an object from being mutated.
------------------------------------------

 Arrow function
 An arrow function is a concise way to write a function expression. It is written with the
 syntax ()=>{code}. Arrow functions are often used as callbacks or when you need to create
 a small, one-time-use function.


 like
 var add = (a, b) => a + b;
 ------------------------------------------

Rest operator
 The rest operator is used to get the rest of the elements in an array or object. It is
 denoted by three dots (...). It is often used in function parameters to get the rest of the
 arguments.
 ------------------------------------------

  grabbing a html element in JavaScript

  there are various ways of doing This
  1. document.getElementById("id") ----class if class----
  2. document.querySelector("selector") ----#selector if id .selector if class----
  3. document.querySelectorAll("selector")```
  ------------------------------------------

````
