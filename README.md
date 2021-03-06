<p align="center">
<img src="https://user-images.githubusercontent.com/103118542/163263986-b74ed5c3-9566-4f10-a328-2a88a1ab5b3a.svg" width="400">
</p>

# UnitConverted.com

<span><img src="https://img.shields.io/badge/Adobe%20XD-470137?style=for-the-badge&logo=Adobe%20XD&logoColor=#FF61F6" /> </span>
<span><img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" /> </span>
<span><img src="https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white" /> </span>
<span><img src="https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E" /> </span>

UnitConverted.com is a free unit converter where you can easily convert all common types
of units: length, temperature, area, volume, weight, time, and speed. It is a super
helpful tool if you expect to have some units converted fast. In addition, you can read
the definitions of each unit with direct reference to scientific sources.

Live app ➡️ https://unitconverted.com

## Case Study

The goal of this project was to design and build an application. I chose to develop a Unit Converter from scratch.
I wanted to challenge myself and try to build a scalable application, a size, and complexity which would be difficult for any novice programmer.

I did my best and worked diligently to accomplish this project.
I am aware that this app could have been done better.
However, my goal in developing this app was to challenge myself, as a beginner, to design a modern interface and to develop it from scratch. I am happy with the final result and would appreciate it if you would read my case study. All suggestions are welcome.

## Project Timeline

I was excited to develop this application. I would like to underline, that the shown
project timeline is real - not fake. The entire application development process went
successfully as intended. However, this was constant work, around 8 hours/day, 6
days/week.

<p align="center">
<img src="https://user-images.githubusercontent.com/103118542/163339916-b4a0d213-9c55-4171-8347-4111712554fa.png">
</p>

## Programming problems to solve

 <ul>
            <li>program the category search filter</li>
            <li>
              write functions that will convert a user input value and return converted value when the "convert" button is clicked
            </li>
            <li>
              program select options so a user can change units easily in the app's interface
            </li>
            <li>
              access DOM elements to display dynamically a calculation result and formula of calculation on the screen
            </li>
          </ul>

## General designing concepts

- get away from the classic bright color scheme
- modern and clean UI
- easy to navigate interface
- design that is memorable and stands out from competing applications

<p align="center">
<img src="https://user-images.githubusercontent.com/103118542/163340737-39d7a0d8-17fe-4f9e-a51b-ff47f48d661a.jpg">
</p>
<p align="center">
<img src="https://user-images.githubusercontent.com/103118542/163340857-305d2093-8bd8-4074-8c8c-e6a5dfb6b95f.jpg">
</p>

## Files management

It's all great as long as you deal with a few files you might probably skip this part.
This time I needed to prepare myself for over 50 files.

Files management was necessary to organize the development part. This app is
scalable which means that anytime it can be further developed - new categories, units and
functionality added.

It is great if you open your app folder and can figure out fast what is what and
get to work without wasting time. It was a part of my plan.

<p align="center">
<img src="https://user-images.githubusercontent.com/103118542/163340960-49212509-5746-4f1f-a7e0-2a7497a74d62.png">
</p>

## SCSS - CSS - files management

You might ask me why did I choose to write styles in SCSS. Well, I find it way more
comfortable to divide styles into seperate files. I mean to divide it logically and
smart. This helps to organize code and just work faster. I love SASS and I think it's a
powerful tool.

I also believe that SASS helps me to follow the Don't repeat yourself principle. I guess,
I've done a pretty good job in this project, not repeating styles by creating plenty of
style cascades.

As browsers do not read SCSS files, all SCSS code was compiled to CSS with the help of
VS Code extension called 'Live Sass Compiler' by Glenn Marks. When the first line of
scss code is written, and 'Watch Sass' is clicked, the extension automatically creates
style.css file and all SCSS code is compiled to clean CSS. I have made some general
changes in the VS Code file called settings.json, where I requested also to create
.min.css (minified version). I also requested to create a new path where all of my .css
files will be initially created. (./public/css).

```
"liveSassCompile.settings.formats": [
{
"format": "expanded",
"extensionName": ".css",
"savePath": "./public/css"
},
{
"extensionName": ".min.css",
"format": "compressed",
"savePath": "./public/css"
}
],

```

I have 4 scss files: style.scss, \_globalStyles.scss, \_desktopDefault.scss, \_breakpoints.scss.

style.scss file has 3 lines of code where I import \_globalStyles.scss,
\_desktopDefault.scss, \_breakpoints.scss, with the help of @use syntax. I used @use
instead of @import since I've read that @import syntax might not be supported anymore,
being replaced by @use.

```SCSS
@use './globalStyles';
@use './desktopDefault';
@use './breakpoints';
```

\_globalStyle.scss is the file that contains general repeatable styles used throughout
the entire project. What do I mean by repeatable styles ?

I set style properties for navs (h1-h4), p tag, a tag, ul, assign default colors to
:root, set properties such as box-sizing to border-box, padding, margin to 0. I created
styles that I assigned to html and body. Basically, this file includes very general
styles. If any of these styles will need to be changed later, I can easily just override
any of them in the .desktopDefault file or .breakpoints file.

```SCSS
* {
box-sizing: border-box;
padding: 0;
margin: 0;
}

:root {
--clr-lightBlue: #40bac2;
--clr-darkBlue: #056b78;
--clr-blueBackground: #0c052d;
--clr-greyBackground: #242424;
}

html {
font-size: 62.5%;
font-family: 'Raleway', sans-serif;
color: white;
background: linear-gradient(#202020, #0c052d);
line-height: 35px;
}

etc.

```

\_desktopDefault.scss are basically the project styles.

\_breakpoints.scss file contains actually breakpoints. I initially set 5 breakpoints.

## Breakpoints

I initially set 5 breakpoints.

<ul>
            <li>max-width: 1199.98px</li>
            <li>max-width: 991.98px</li>
            <li>max-width: 767.98px</li>
            <li>max-width: 575.98px</li>
            <li>max-width: 320px</li>
          </ul>

<p>
            However, the first breakpoint (1199.98px) was unnecessary so I removed it and started
            responsive styling from the breakpoint of max-width: 991.98px. Most of the changes were
            done in the breakpoint of max-width: 575.98px.
          </p>
          <p>
            I also created some extra tags in the HTML, to make this app 100% mobile-friendly. These
            tags got hidden for desktop/laptop/tablet versions and are visible only in a mobile
            version.
          </p>
          <p>
            For example &lt;p&gt; tag with the class of 'from' was replaced by a &lt;p&gt; tag with the
            class of 'fromMobile'. You may ask me why did I do it?
          </p>
          <p>
            Well, the problem was that a &lt;p&gt; tag with the class of 'from' was in a &lt;div&gt;
            that has a 'flex' property set. This made it impossible to style on mobile to the point,
            where I wanted to let it be. That's why I created a new &lt;p&gt; tag and I grabbed it
            out of that &lt;div&gt; and moved it to the top. I hope you understand what I mean.
          </p>

```HTML
<div class="converterWrapper">
<p class="fromMobile">From:</p>
<div class="converterInternalWrapper1">
<p class="from">From:</p>
<input class="inputUnit" type="number" placeholder="write numbers" />
<select name="unitsFrom" class="unitsFrom">
<option value="frommm" class="frommm">millimeter</option>
<option value="fromcm" class="fromcm">centimeter</option>
<option value="fromm" class="fromm">meter</option>
<option value="fromkm" class="fromkm">kilometer</option>
<option value="frommile" class="frommile">mile</option>
<option value="fromyard" class="fromyard">yard</option>
<option value="fromfoot" class="fromfoot">foot</option>
<option value="frominch" class="frominch">inch</option>
</select>
</div>

```

  <p align="center">
<img src="https://user-images.githubusercontent.com/103118542/163342255-e1577b4d-add3-48ce-9cb3-500e34dba344.png">
</p>
  
 ## JavaScript project files
I decided to create 3 .js files: main.js, functions.js, and components.js. The
            proper division of files allowed me to keep the project in order and in case of any
            changes I would be able to do it intuitively and quickly.

The main.js file contains querySelectors that allow accessing DOM elements, event
listener (convert button), for loops (looping both select option windows), with multi if
statements that call a particular function if a given condition is met by a user.

The functions.js file is individual functions written for each unit conversion that
returns the value of the expression. All of these functions are exported and imported into
the main.js file.

The components.js file is the file that contains some individual components of the
application that are duplicated and appear in multiple places on the interface. I
created components like footer, unit lists, search-wrapper, with the idea that in the
future if I want to apply changes, I don't have to edit in dozens of places in the
application but I can edit it from one place, and the changes will automatically appear
everywhere. Components are sort of like re-usable templates.

## Programming problems solving - JS concepts

<b>1. The category search filter</b>

 <p>
                The category search filter is the application component that is imported in the HTML sheet
                &lt;search-wrapper class="searchWrapper"&gt; &lt;/search-wrapper&gt;.
              </p>
              <p>This problem was solved easily.</p>
              <p>
                I accessed DOM element &lt;select&gt; with the given class of 'categories'
                adding this element to the variable named 'categories'.
              </p>
              <p>
                I accessed DOM element &lt;button&gt; with the class of 'find' and attached an Event
                Listener on 'click', with a callback function, passing no parameters.
              </p>
              <p>
                I created a mutable variable 'let' and named it as the 'options'. I assigned to the variable
                'options', the variable 'categories', adding property 'selectedOptions'.
              </p>
              <p>
                I ran a for loop that looped through the 'options', giving me access to selected option
                by a user. Once a user chooses a specific category and clicks on the 'find' button,
                a category page will open.
              </p>
  
   <p align="center">
<img src="https://user-images.githubusercontent.com/103118542/163351949-92023267-8a93-4a3a-923a-445cd50db0ce.jpg" width="300">
</p>


```Javascript
export const categories = document.querySelector('.categories');

export let categoriesBox = document.querySelector('.find').addEventListener('click', function () {
let options = categories.selectedOptions;
for (let i = 0; i < options.length; i++) {
window.open(options[i].value, '_self');
}
});

```

<b>2. Functions that convert a user input value</b> <br>
I wrote an arrow function and passed the parameter 'inputValue'. The 'InputValue' is basically
whatever a user will write in the input field.

```Javascript
// Decimal numbers are NOT rounded

//---------------------------------------
//LENGTH CONVERTER FUNCTIONS

export const mmToCm = (inputValue) => {
return inputValue / 10;
};
```

As the 'inputValue' parameter is a DOM element, I accessed this element with a basic line of
code. I made sure, that any number written in the input field will be converted to a
"Number", instead of being a 'String'. By default, any content in the input field is
treated as a "String".

```Javascript
const input = Number(document.querySelector('.inputUnit').value);
```

 <p>
            A certain function gets invoked, when condition is met, which means that in
            &lt;select&gt; &lt;option&gt; user picked to convert mm to cm. The name 'calc' is added
            initially to each function because I imported to main.js all of the functions from a
            functions.js file and named that import as 'calc'.
          </p>

So the function is invoked that way.

```Javascript
calc.mmToCm(input);
```

<b>3. Program select options so a user can change units easily in the app's interface</b>
<p>
Select options are basically some units. There are 2 &lt;select&gt; tags with
&lt;options&gt; in the HTML sheet. User can decide what units should be converted.
</p>

<img src="https://user-images.githubusercontent.com/103118542/163361899-5cef5654-d6ff-4cfe-a4ab-35e5f6711b9f.png">
        


```Javascript
<div class="converterWrapper">
<p class="fromMobile">From:</p>
<div class="converterInternalWrapper1">
<p class="from">From:</p>
<input class="inputUnit" type="number" placeholder="write numbers" />
<select name="unitsFrom" class="unitsFrom">
<option value="frommm" class="frommm">millimeter</option>
<option value="fromcm" class="fromcm">centimeter</option>
<option value="fromm" class="fromm">meter</option>
<option value="fromkm" class="fromkm">kilometer</option>
<option value="frommile" class="frommile">mile</option>
<option value="fromyard" class="fromyard">yard</option>
<option value="fromfoot" class="fromfoot">foot</option>
<option value="frominch" class="frominch">inch</option>
</select>
</div>
<p class="toMobile">To:</p>
<div class="converterInternalWrapper2">
<p class="to">To:</p>
<select name="unitsTo" class="unitsTo">
<option value="tocm" class="tocm">centimeter</option>
<option value="tomm" class="tomm">millimeter</option>
<option value="tom" class="tom">meter</option>
<option value="tokm" class="tokm">kilometer</option>
<option value="tomile" class="tomile">mile</option>
<option value="toyard" class="toyard">yard</option>
<option value="tofoot" class="tofoot">foot</option>
<option value="toinch" class="toinch">inch</option>
</select>
<button class="convertBtn">CONVERT</button>
</div>
</div>
```

 <p>To access by class &lt;select&gt; in DOM, I simply wrote the code.</p>  
            
 ``` Javascript
 let unitsFrom = document.querySelector('.unitsFrom');
let unitsTo = document.querySelector('.unitsTo');
```            
<p>
           To access options (&lt;option&gt; tag) inside the &lt;select&gt;, I created the
            variables 'options1' & 'options2' and assigned to them created before variables such as
            unitsFrom & unitsTo, with the property 'selectedOptions'.
          </p>
          <p>
            Then I created a for loop inside another for loop and looped through the 'options1' and
            'options2' gaining access to each individual &lt;option&gt;.
          </p> 
          
 ``` Javascript
 ...
let options1 = unitsFrom.selectedOptions;
let options2 = unitsTo.selectedOptions;

for (let a = 0; a < options1.length; a++) {
console.log(options1[0]);
for (let b = 0; b < options2.length; b++) {
console.log(options2[0]);
...

````
How does the browser know what units a user choose ? I created if conditions (inside 2
            for loops) where I pointed the first looped element among 'options1' & 'options2', which
            is the 'options1[0]' & 'options2[0]'. Just a reminder that robots count from 0 instead of 1.

Logically, the chosen unit by a user will always be the first one - [0].

Based on if statements the browser knows what to do and what functions should be invoked.

``` Javascript
if (options1[0] === frommm && options2[0] === tocm) {
output =
`${input} ` + `${options1[0].textContent}` + ' = ' + calc.mmToCm(input) + ` ${options2[0].textContent}`;
document.querySelector('.conversionResult').textContent = output;
document.querySelector('.formula').textContent = `Formula: ${input} ${options1[0].textContent} divided by 10 `;
}
````

<b>4.Access DOM elements to display dynamically the calculation result and formula on the screen</b> <br>
<img src="https://user-images.githubusercontent.com/103118542/163362630-c5922ea0-aa5b-4e7c-9d25-69b985d28206.jpg">

<p>
            There are 2 empty &lt;p&gt; tags created in the HTML sheet with a class of
            'conversionResult' and 'formula'.
          </p>


```
<p class="conversionResult"></p>
<p class="formula"></p>
```

I created the empty variable 'output'. The result of conversion is based on the if
condition and its function is assigned to the variable 'output'. A mutable value that
'output' variable contains, gets assigned to DOM element with a class of
'conversionResult' with an added property of 'textContent'. The result conversion will
be dynamically displayed in the &lt;p&gt; tag.

'Formula' was done the same way, excluding assigning output. I accessed DOM element with
a class of 'formula' and assigned a string with dynamic fields such as 'input' and
'options1'.

```
if (options1[0] === frommm && options2[0] === tocm) {
             output =
               `${input} ` + `${options1[0].textContent}` + ' = ' + calc.mmToCm(input) + ` ${options2[0].textContent}`;
             document.querySelector('.conversionResult').textContent = output;
             document.querySelector('.formula').textContent = `Formula: ${input} ${options1[0].textContent} divided by 10 `;
           }
```

## Problems I encountered during the development process

Honestly, I didn't encounter many problems while coding. To a surprise, with a little
bit of analyzing I was actually able to match javascript concepts very fast to solve any
problems. However, I got stuck for a while styling website ...

<b>SCSS and nested classes</b>  
What I love about SCSS are nested classes. I just find it comfortable to create some
sort of "class trees". I say it's comfortable because anytime I am back to a specific
class to add some extra styling, someway I can easily locate this class, without using
the built VS Code 'search' tool. Certainly, there are other advantages of nesting
classes such as clean code and not having to repeat code. For example, if div with a
class of 'flex' is inside a div with a class of 'wrapper', and there's a &lt;p&gt; tag
inside that div 'flex', you may write it that way.

```
.wrapper {

            .flex {

            p { }

            }

            }

            //instead of

            .wrapper {}

            .flex p {}

            .flex {}
```

However, nested classes can be tricky especially when you want to override some styles.
That's what I experienced.

I tried to override some styles, especially doing media queries, and even though I added
styles to a certain HTML element with a class of 'x', the results were not displayed in
the browser. I was confused about why the styles are not
overridden.

Well, it's all because I ignored initially declared nested classes. What I mean, based
on the random example given above is if you declared initially div with a class of
'flex' to be nested inside the 'wrapper', the compiled result of this nesting in the
style.css sheet will be:

```
.wrapper .flex {}

 .wrapper .flex p {}
```

So in fact if you want to override any styles doing for example media queries, you
should use previously declared nested classes.

## Overall feelings

I am happy that I was able to write my first application. It is not something innovative, but it
is mine, from A to Z written by me. I am full of motivation to keep working hard. More
projects coming soon. Thank you for reading.

## Contributing

Contributing to this project is very welcome. Please send an inquiry.
