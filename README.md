# HTML

---
### Intro
- elements
    - start & end tags `<tagname>Content goes here...</tagname>`
     - attributes
        - style 
            - <tagname style="property: value;">
            - background-color defines background color
            - color property defines text color 
            - font-family
            - font-size
            - text-align
        - lang ( important for accesibility app & search engine) 
        - title ( tooltip ) 
    - browser do no display html tags, it renders the content 
    - <!Doctype> represents the document type and helps browsers to display web pages correctly
    - case insensitive 
    - empty elements - <br/>, doesn't contain any content
    
    
### Topics
##### heading
 - h1 - h6
 - font-size attribute to make the header bigger
##### paragraph
 - end closing tag
 - doesn't work with space, new line in single paragraph
 - to solve poem problem use < pre> tag which defines pre-formatted text
##### links
 - color
  - can be changed with a:link, a:visited, a:hover, a:active styling 
 - target
  - _blank ( new tab or window) 
  - _self 
  - _parent ( parent frame ) 
  - _top ( full body of window)
  - framename
 - Create a Bookmark
  ```
   <p id="c4"> chapter 4 </p>
   < a href="#c4"> Jump to chapter 4</a>
   < a href="page_name.html#c4"> Jump to chapter 4</a>
  ```
  
##### images 
   - attribute
        - src
        - alt 
        - width
        - height
     - style
       - width, height 
       - float
       - background-image:url('image_path')
     - map ( cn create clickable areas in image ) 
     - `<picture> <source media = "(min-width:560px)" srcset="file_path"> (in html 5 multiple photo with resizing change) `
      
##### buttons
  - button
##### lists
 - unordered(ul), ordered(ol)
 - style="list-style-type: disc" / circle, square, none
 - type="1"
 - description list 
     - <dl><dt>Title</dt><dd>definition</dd></dl>
 - start="50"
 
##### Tables
 ```<table><caption>C</caption><tr><th></tr><tr><td></td></tr></table>``` 
 - th by default center bold
 - style 
  - table, th, td{ border: 1px solid black; border-collapse: collapse;}
  - th, td{padding: 15px}
  - rowspan, colspan
  - table#t01 tr:nth-child(even) {background-color: #eee;}
  
##### formatting elements
 - b 
 - strong ( same as b)
 - i
 - em ( almost same as i)
 - mark ( mark text ) 
 - small
 - del
 - ins ( underlined ) 
 - sub
 - sup
 - q (quotation mark around p ) 
 - blockquote cite="url"
 - address ( italic address) 
 - cite( italic ) 
 - bdo dir="rtl" (text direction right to left ) 
##### Comments
 ```<!-- comments -->``` 
##### Colors
 - style="border: 2px solid Tomato"
 - Color Value
  - rgb(255,99,71)
  - `#ff6347`
  - hsla(9, 100%, 64%, 0.5)  - hue, saturation, lightness
   - hue
      - 0 red
      - 120 green
      - 240 blue
   - saturation
    - intensity ( 100% pure color, 50% gray can see, 0% completely gray cannot see)
   -lightness
    - 0% black, 50% neither dark nor light, 100% lightness white
  -rgba(255,99,71, 0.5)  - transparent 50% (rgba(red,green,blue,alpha))
   - alpha 0.0(full transparent, 1.0(not transparent at all) 
### Best Practices
- lower case 
- quotes
    - single/double both fine
##### Style
 - can be added 3 ways
  - inline
  - internal
  - external
   ` <link rel="stylesheet" href="style.css">`
  - border
    - border around html element
   - padding
   - space between text and border
  - margin
   - margin outside the border
  - id
   - one special element
  - class
   - for all special types of elements
   
##### Blocks
 - block-level element always starts on a new line and takes up the full width available 
 - inline elements - *does not start on a new line*  
     - span
      - helpful to style parts of text **
     - div 
      - helpful to style blocks of content 
##### Class Attribute
 - styling 
 - html elements can have more than one class 
 - different tag can share same class 
 - in JS getElementByClassName() method can access specified class 
##### Id Attribute 
 - unique 
 - can be used by css & js
     - in css #
 - case sensitive 
 - at least one character and no whitespace allowed
 - id vs class
   - id once used but class can be used multiple time
 - getElementById("idName") can be used in JS
 
##### Iframe
 - Webpage within another webpage
 - `<iframe src="url"></iframe>`
 - height/width same as img
 - iframe 'target' attribute can be used to target frame for a link

##### HTML Javascript
 - make pages more dynamic and interactive 
 - script 
 - document.getElementyById("idName").*
    - innerHTML
    - style.color
    - src
 - noscript tag used to notify user that js is not supported or disable

##### HTML File Paths
 - absolute, relative path
##### HTML Head Element
 - container for metadata 
   - metadata contains title, style, links, script, base 
 - `<meta>` tag is used by the browser to display content, by search engines and other web services
   - description of website
   - refresh web-page every 30 second
   - author name 
   - viewport
     - varies with the device to control web-page content
##### HTML Layout
  - table
  - float
  - flexbox
  - grid
  - framework

##### HTML Responsive 
  - viewport
  - responsive image
    - width - scaled greater than original size 
    - max-width - scaled upto original size 
    - `<picture> <source media = "(min-width:560px)" srcset="file_path"> (in html 5 multiple photo with resizing change) `
  - responsive text size 
    - text size in 'vw' (viewport width)
  - media queries 
    - media queries you can define completely different styles for different browser sizes.
        ``` 
        
            /* Use a media query to add a breakpoint at 800px: */
            @media screen and (max-width: 800px) {
              .left, .main, .right {
                width: 100%; /* The width is 100%, when the viewport is 800px or smaller */
              }
            }
        ```
  - use bootstrap or other CSS framework 
  
##### Computer Code 
   - code
     - use pre outside code as code doesn't contain formatting
   - kbd - keyboard
   - samp - output from a program or computer system
   - var - variable
##### HTML Entities
  - &lt otr &#60
  - &nbsp; - non breaking space 
  - &gt
  - &quot
  - &amp
##### HTML Symbols
  - different mathematical & greek symbol
  - [See for Details](https://www.w3schools.com/html/html_symbols.asp)
  
##### HTML Encoding 
  - to understand a browser which character set to use  
  - `<meta charset="UTF-8">`
  
##### HTML XHTML
  - extensible hyper text markup language
  - elements
    - must properly nested
    - must close
    - must lower case
    - must one root
  - attributes
    - lower case
    - quoted
  -Doctype
    - mandatory
    - xlmns attribute mandatory  
##### HTML Forms
  - `<form>`
    - action
    - target
        - _self
        - _blank (new tab)
        - _parent
        - _top
    - method
      - get
      - post 
  - `<input>`
    - type 
        - radio
        - text
        - password
        - submit
        - reset 
        - checkbox
        - in html5 
          - color
          - date
          - datetime-local
          - email
          - file
          - month 
          - number 
          - url 
          - time
          - week 
          
    - name
    
  - select
    - name
        - option
          - value
  - textarea
    - rows, cols 
    - height, width
    
  
  - fieldset tag
    - group data
    - legend tag give title to fieldset
    
  - form attributes 
    - disabled
    - size 
    - maxlength 
    - autocomplete
    - novalidate 
    - placeholder
    - required 
    - autofocus
    

# JS

---
```javascript
//parseint cannot work if format is string_number, in this case it provide NaN but works in number_string format


<!DOCTYPE html>
<html>
<head>
    <title>JavaScript</title>
    <!-- external from file system -->
    <script src="hello.js"></script>
    <!-- external from cdn -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
</head>
<body>

    <!-- inner text change to time -->
<button type="button" onclick="document.getElementById('demo1').innerHTML = Date()">Press Me baby to see present time!!!</button>
<p id="demo1">Time will be shown here ... if upper button pressed</p>

<!-- inner text change -->
<button type="button" onclick='document.getElementById("demo2").innerHTML = "Hello JavaScript!"'>Click Me </button>
<p id="demo2">I will be changed when button clicked </p>

<!-- image change -->
<button onclick="document.getElementById('myImage').src = 'pic_bulboff.gif'">Turn Off Light</button>
<button onclick="document.getElementById('myImage').src = 'pic_button.gif'">Turn on Light</button>
<img src='pic_bulboff.gif' id="myImage">


<br/>
<!-- inner text manipulation -->
<button type="button" onclick="document.getElementById('demo3').style.fontSize = '35px'"> Click Me to change font size </button>
<p id = "demo3">My Size Will be chaged if the upper button pressed</p>

<!-- hide any element -->
<button type="button" onclick="document.getElementById('demo4').style.display='none'"> Click Me to hide</button>
<p id = "demo4">I will be deleted from the earth if the upper button pressed</p>


<!-- show and hidden element -->
<button type="button" onclick="document.getElementById('demo5').style.display='block'">Press to see what is waiting for you..!!!</button>
<p id="demo5" style="display:none">Boooooooooooooooo!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!</p>


<!-- JavaScript Display Possibilities -->
<!-- innerHTML, document.write(), window.alert(), console.log() -->

<!-- document.write() --><br/>
<script>document.write("i am from document write");</script>

<!-- i am from onclick and document. write --><br/>
<button type="button" onclick="document.write('everything deleted :( ')"> Dont Press !!! I will delete everything!!</button>

<!-- i am from window.alert -->
<script>
    // window.alert('Hello from Alert!!!');
</script>

<!-- i will be printed on console -->
<script>
    console.log("I am in console...!!");
</script>

<!-- JS statements --><br/>
<p>The following line is set from js-</p>
<p id='demo8'></p>
<script>var x,y,z; x = 5 ; y = 6; z = x + y; document.getElementById('demo8').innerHTML = z;</script>
<!-- JS code order matters!!!! -->

<!-- array of objects -->
<script>
    var cars = [
        {type:"Volvo", year:2016},
        {type:"Saab", year:2001},
        {type:"BMW", year:2010}
    ];
</script>

<!-- form validate --><br/>
<form name="myForm" action="/action_page.php"
onsubmit="return validateForm()" method="post">
Name: <input type="text" name="fname">
<input type="submit" value="Submit">
<script>
    function validateForm() {
    var x = document.forms["myForm"]["fname"].value;
    if (x == "") {
alert("Name must be filled out");
        return false;
}
}

// getting value of a variable
x = document.getElementById("numb").value;

</script>
<!-- html default required field -->
<input type="text" name="fname" required>

<!-- loop -->
<p id="demo10"></p>
<script>
        var txt = "";
        var person = {fname:"John", lname:"Doe", age:25};
        var x;
        for (x in person) {
            txt += person[x] + " ";
            document.write("name: " + x + "<br/>");
            document.write("value:" + " " + person[x] + "<br/><br/>");
        }
        document.getElementById("demo10").innerHTML = txt;
</script>


<!-- function inside object -->
<p id="demo11"></p>
<script>
        var person = {
            firstName: "John",
            lastName : "Doe",
            id : 5566,
            fullName : function(hoga) {
             return this.firstName + " " + this.lastName + " " + hoga;
            }
        };
        document.getElementById("demo11").innerHTML = person.fullName("billaal");
</script>

<!-- adding function to an object -->
<p id="demo12"></p>
<script>
        var person = {
            firstName: "John",
            lastName : "Doe",
            id : 5566,
        };
        person.name = function() {
            return this.firstName + " " + this.lastName;
        };
        
        document.getElementById("demo12").innerHTML =
        "My father is " + person.name();
        </script>

<!-- constructor -->
<p id="demo13"></p>

<script>

// Constructor function for Person objects
function Person(first, last, age, eye) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eye;
}

// Create a Person object
var myFather = new Person("John", "Doe", 50, "blue");

// Display age
document.getElementById("demo13").innerHTML =
"My father is " + myFather.age + ".";

</script>


<!-- JS closures -->
<script>
    var add = (function () {
    var counter = 0;
    return function () {return counter += 1;}
})();

add();
add();
add();
//This is called a JavaScript closure. It makes it possible for a function to have "private" variables.
// the counter is now 3
</script>

<!-- DOM

it is object model and programming interface, 
- element as object
- properties of all html elements
- methods to access all html elements
- events for all html elements

=> standard for how to get, change, add or delete html elements

DOM - methods => actions performed on html elements
DOM - properties => value that can set or change
document.getElementById("demo").innerHTML = "Hello World!";
getElementById -> method
innerHTML -> property

Finding HTML elements -
    document.getElementById(id)
    document.getElementsByTagName(name) // return array of all elemnts with the tag
    document.getElementsByClassName(name) // also return an array

    var x = document.querySelectorAll("p.intro"); // return <p> elements with class "intro"

Changing HTML Elements - 
    element.innerHTML - new html content
    element.attribute - new value
    element.setAttribute(attribute, value)
    element.style.property = new style

Adding or deleting Elements- 
    document.createElement(element)
    document.removeChild(element)
    document.appendChild(element)
    document.replaceChild(element)
    document.write(text)

Adding Event Handlers
    document.getElementById(id).onclick = function(){//somecode}



<p id="myBtn">Try it</p>
    document.getElementById("myBtn").addEventListener("click", displayDate);

-->



<!-- creating new element by DOM -->
<div id="div1">
    <p id="p1">This is a paragraph.</p>
    <p id="p2">This is another paragraph.</p>
    </div>
    
    <script>
    var para = document.createElement("p");
    var node = document.createTextNode("This is new.");
    para.appendChild(node);
    
    var element = document.getElementById("div1");
    var child = document.getElementById("p1");
    element.insertBefore(para,child);
    </script>


<!-- redirect to new page -->

<script>
    function newDoc() {
        window.location.assign("https://www.w3schools.com")
    }
    </script>

    <!-- cookie -->
    <!-- 
        Cookies are data, stored in small text files, on your computer.
        When a web server has sent a web page to a browser, the connection is shut down, and the server forgets everything about the user.
     -->
    <!-- 

        cookie can be created, read, changed, deleted by JS
     -->




     <!-- AJAX -->
     <!-- 

        AJAX is a developers dream, because you can:

Read data from a web server - after the page has loaded
Update a web page without reloading the page
Send data to a web server - in the background
     -->




<!-- Already Known Topics -->
<!-- 
Syntax
Comments
Variables

 -->


 <!-- some basic topics -->
 <script>
     var x = "5" + 2 + 3 ;
     //output is 523 , if a number string then whole string but if 2 + 3 + "5" then it will print 55 actually it works from left to right
    // "2" > "12"  true
     var charName = "bugetti";
     var charName;
     //now printing charName is "bugettin" for javascript
     var notAssigned; // it will print undefined; 

     // **  Exponentiation
    //     >>> Shift right (unsigned)
    // ===  Strict equal
    // 
 </script>


<!-- script can be written within script tag --><br/>
<p id="demo6"></p>
<p id ="demo7" onclick="changeText()">I will be change when clicked by me..</p>



</body>
<script>
    // Scripts can be placed in the <body>, or in the <head> section of an HTML page, or in both.
    // You can place any number of scripts in an HTML document.

    document.getElementById('demo6').innerHTML = "hello from script tag";
    function changeText(){
        document.getElementById('demo7').innerHTML = ' I am changed :( by clicking ';
    }
</script>
</html>



======================================================
-string can be both with '' and " " ; 
-array declared with [] and object declared with {}
-do not create global variable if not needed 
-string concatination with + 
-splice() method can add or delete element from array
-slice() method create new array


In JavaScript there are 5 different data types that can contain values:

string
number
boolean
object
function
There are 3 types of objects:

Object
Date
Array
And 2 data types that cannot contain values:

null
undefined




ECMAScript 6 / JS 6
let keyward - 
var x = 10;
// Now x is 10
{ 
    let x = 2;
    // Now x is 2
}
// Now x is 10

--
var x = 10;
// Now x is 10
{ 
    const x = 2;
    // Now x is 2
}
// Now x is 10
constant similar to let, except that the value of the variable cannot be changed.

function default parameter - 
function myFunction(x, y = 10) {
    // y is 10 if not passed or undefined
    return x + y;
}
myFunction(5); // will return 15
new methods - 
isFinite()
isNan 
Arrow Function - 

 dont need the function keyword, the return keyword, and the curly brackets.
// ES5
var x = function(x, y) {
     return x * y;
}

// ES6
const x = (x, y) => x * y;

All numbers in JavaScript are stored as 64-bits Floating point numbers (Floats).


JS Function
function functionName(parameters) {
  code to be executed
}
A function expression can be stored in a variable:
var x = function (a, b) {return a * b};
var z = x(4, 3);
The function above is actually an anonymous function (a function without a name). They are always invoked (called) using the variable name.

Self Invoking function - 
(function () {
    var x = "Hello!!";      // I will invoke myself
})();
Argument - 
x = sumAll(1, 123, 500, 115, 44, 88);

function sumAll() {
    var i;
    var sum = 0;
    for (i = 0; i < arguments.length; i++) {
        sum += arguments[i];
    }
    return sum;
}

call and apply - 
The call() method takes arguments separately.

The apply() method takes arguments as an array.

else everything is same.

var person = {
    fullName: function(city, country) {
        return this.firstName + " " + this.lastName + "," + city + "," + country;
    }
}
var person1 = {
    firstName:"John",
    lastName: "Doe",
}
person.fullName.apply(person1, ["Oslo", "Norway"]);

person.fullName.call(person1, "Oslo", "Norway");








JS Object:
Objects are variables. But objects can contain many values.

The values are written as name : value pairs (name and value separated by a colon). The name is called property. 

Objects are mutable: They are addressed by reference, not by value.

var person = {
    firstName: "John",
    lastName : "Doe",
    id       : 5566,
    fullName : function() {
        return this.firstName + " " + this.lastName;
};
//this refers to the "owner" of the function.
//If you access the fullName property, without (), it will return the function definition
var x = person;       // This will not create a copy of person.
x.age = 10;           // This will change both x.age and person.age

loop in object - 
for (x in person) {
    txt += person[x];
}

person.nationality = "English";    // adding new property 
delete person.age;   // or delete person["age"]; 

//Constructor 
function Person(first, last, age, eyecolor) {
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eyecolor;
}
var myFather = new Person("John", "Doe", 50, "blue");
var myMother = new Person("Sally", "Rally", 48, "green");

The JavaScript prototype property also allows you to add new methods to objects constructors:

Person.prototype.name = function() {
    return this.firstName + " " + this.lastName;
};

JS HTML DOM 
JavaScript can change all the HTML elements in the page
JavaScript can change all the HTML attributes in the page
JavaScript can change all the CSS styles in the page
JavaScript can remove existing HTML elements and attributes
JavaScript can add new HTML elements and attributes
JavaScript can react to all existing HTML events in the page
JavaScript can create new HTML events in the page
The HTML DOM is a standard object model and programming interface for HTML. It defines:

The HTML elements as objects
The properties of all HTML elements(like changing the content of an HTML element).
The methods to access all HTML elements (like add or deleting an HTML element).
The events for all HTML elements
In other words: The HTML DOM is a standard for how to get, change, add, or delete HTML elements.

Access HTML Element - getElementById(),getElementByTagName(),getElementByClassName()

Get content of element - innerHTML()

Changing HTML Elements - 

    element.innerHTML

    element.attribute

    element.setAttribute(attribute,value)

    element.style.property = new style

Adding and Deleting Element- 

document.createElement(element)	Create an HTML element
document.removeChild(element)	Remove an HTML element
document.appendChild(element)	Add an HTML element
document.replaceChild(element)	Replace an HTML element
document.write(text)	Write into the HTML output stream
Adding Event handlers -

document.getElementById(id).onclick = function(){code}	Adding event handler code to an onclick event
Object Collection - 

document.anchors
document.body
document.documentElement
document.embeds
document.forms
document.head
document.images
document.links
document.scripts
document.title  
Chanting attribute value - 
document.getElementById(id).attribute = new value
Chanting HTML style - 
document.getElementById(id).style.property = new style
JavaScript HTML DOM events - 

onclick=JavaScript

Adding Event Listener - 

element.addEventListener("click", myFunction);

Accessing the innerHTML property is the same as accessing the nodeValue of the first child

var myTitle = document.getElementById("demo").firstChild.nodeValue;

Create - Replace - Delete Node - 

<div id="div1">
<p id="p1">This is a paragraph.</p>
<p id="p2">This is another paragraph.</p>
</div>

<script>
var para = document.createElement("p");
var node = document.createTextNode("This is new.");
para.appendChild(node);

var parent = document.getElementById("div1");
var child = document.getElementById("p1");
parent.replaceChild(para, child);



child = document.getElementById("p1");
child.parentNode.removeChild(child);
</script>

Dom List Lenght: 

var myNodelist = document.querySelectorAll("p");
document.getElementById("demo").innerHTML = myNodelist.length;



JS Timing - 

var myVar = setInterval(myTimer, 1000);

function myTimer() {
    var d = new Date();
    document.getElementById("demo").innerHTML = d.toLocaleTimeString();
}

<button onclick="myVar = setTimeout(myFunction, 3000)">Try it</button>

<button onclick="clearTimeout(myVar)">Stop it</button>

myVar = setInterval(function, milliseconds);
clearInterval(myVar);



COOKIE - 
<script>

function setCookie(cname,cvalue,exdays) {
    var d = new Date();
    d.setTime(d.getTime() + (exdays*24*60*60*1000));
    var expires = "expires=" + d.toGMTString();
    document.cookie = cname + "=" + cvalue + ";" + expires + ";path=/";
}

function getCookie(cname) {
    var name = cname + "=";
    var decodedCookie = decodeURIComponent(document.cookie);
    var ca = decodedCookie.split(';');
    for(var i = 0; i < ca.length; i++) {
        var c = ca[i];
        while (c.charAt(0) == ' ') {
            c = c.substring(1);
        }
        if (c.indexOf(name) == 0) {
            return c.substring(name.length, c.length);
        }
    }
    return "";
}

function checkCookie() {
    var user=getCookie("username");
    if (user != "") {
        alert("Welcome again " + user);
    } else {
       user = prompt("Please enter your name:","");
       if (user != "" && user != null) {
           setCookie("username", user, 30);
       }
    }
}

</script>

<body onload="checkCookie()">
```


#CSS

---

### Introduction
 - structure
   > selector { declaration;declaration}
     - selector 
       - html element
       - id
       - class
       - specify html element
     - declaration
       - property name : value
       
 - same style definition can be grouped     
 - comments
   - `/* hello */`
### Inserting CSS to html
 - internal 
 - external
 - inline
 
 - the value from last read style sheet will be used for same selector
 
### Color
 - see html cheat sheet 

### Backgrounds
  - background-color
  - background-image
    -  url('filePath')
  - background-repeat
    - repeat-x
    - no-repeat
  - background-position
    - right top;
  - background-attachment
    - fixed 
    
  - shorthand 
    - `background: #ffffff url("img_tree.png") no-repeat right top;`
```
  - border
    - border around html element
   - padding
   - space between text and border
  - margin
   - margin outside the border
```  
  
### Borders
  - border-style
    - dotted
    - solid
    - dashed
    - double
  - border-width
  - border-color
  - border-top-style
  
  - border-radius 
  
  - shorthand
    - `border: 5px solid red`

### Margins
  - margin ( works clockwise in shorthand )
    - top
    - right
    - bottom
    - left
    
    - auto ( horizontally center the element )
    
    - inherit ( to get parent styling)
    
  - shorthand
    - `margin: 25px 50px 75px 100px`
    


### Padding
  - top
  - right
  - bottom
  - left 
  
  - box-sizing: border-box; will retain the size of the box, without using it box resized with padding
  
  > padding & margin are transparent
  
### height/width
  - use max-height to avoid scrollbar 
  
### Box Model
  - content, padding, margin, border consist the box model
  - width & height just cover the content area so the padding & margin need to be added to measure the overall content area
   
### Outline
  - outline-style
  - outline-color
  - outline-width
  - outline-offset(space between element and outline)
  - outline
  
  - shorthand 
    - 5px solid lightgreen
    
### CSS Text
  - color
  - text-align
    - justify 
  - text-decoration
    - none
    - overline
    - line-through
    - underline
  - text-transformation
    - uppercase
    - lowercase
    - capitalize
  - text-indent ( works only in the first line )
  - letter-spacing
  - line-height
  - direction
  - text-shadow
### Font  
  - font-family 
    - "Times New Roman"
    - Times
    - serif
    - monospace
    - sans-serif
  - font-style
    - normal
    - italic
    - oblique
    
  - font-size
    - 1em = 16px 
    - %
    - px 
    > vw (viewport width)
  - font-weight
  - font-variant 
    - small-caps
    - normal
### CSS Icons
  - [font awesome](href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css")
  - [Bootstrap](<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">)
  - [Google Material](<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">)
  
  
### Link
 - a:link
 - a:visited
 - a:hover
 - a:active
 
   - color
   - text-decoration
   - background-color
   
   
      
### List
 - list-style-type
   - circle
   - square
   - upper-roman
   - lower-alpha
 - list-style-image
   - urll('img_path')
 - list-style-position
 - list shorthand
   - > list-style: square inside url('path')
       
### Table
  - border-collapse
  - 1px solid black
  - tr:nth-child(even){style;}
  - tr:hover{style;}
  
  - >> overflow-x: auto
    - makes table responsive
    - ``` 
           <div style="overflow-x:auto;">
           
           <table>
           ... table content ...
           </table>
           
           </div>
      ```
### Display
 - block, inline
   - block element starts on a new line
   - inline doesn't start on a new line
   
   - to display list item in a line
     - li{ display: inline;}
   
 - script tag uses display: none; by default
 - display:none
   - element will be hidden and page won't display the element
 - visibility:hidden
   - element will be hidden but still affect the layout with space 
   
### max-width
 - for responsive resizing  
 
### Position
  - elements are positioned using top,bottom,left,right after setting the positioning method
  
  - static ( by default all elements are)
  - relative
  - fixed
    ``` css
      position: fixed;
      bottom: 0;
      right: 0;
      width: 300px;
      border: 3px solid #73AD21;
    }
    ```
  - absolute
    - works with relative styled element
    
  - z-index: -1, specifies the stack order of an element
  
  - img
    - opacity 
  
  - sticky 
### Overflow
  - visible
  - hidden
  - scroll
  - auto  
    - if overflow clipped then add scrollbar    
    
  - overflow-x: hidden;
    - hide horizontal scrollbar




