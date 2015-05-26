# SASS4beginners
SASS courses for beginners.    
[Reference](https://github.com/ganlanyuan/SASS4beginners/blob/master/reference.md)   
[Screen recording](http://creatiointl.org/gallery/sass-video/)   

### #1 Basis
An introduction to Sass, install, imports, comments, and nesting.     
1. [CSS Preprocessors and Parent Selectorsa](http://davidwalsh.name/stylus-parent-selectors)   

[Slider](http://slides.com/ganlanyuan/deck/#/)

**nesting**
````scss
nav {
  li {
    line-height: 1.3;
    &:hover { background: #dbdbdb; }
  }
  .sub-nav {
    &-1 { background: #f2f2f2; }
    &-2 { background: #dbdbdb; }
    &-3 { background: #f5f5f5; }
  }
}
````

### #2 Use a Framework
Learn to import and use a framwork.   

### #3 Math & Variable
Creation and use of recallable information.  
1. [Choosing great variable names](http://thesassway.com/beginner/variable-naming)   
2. [Stop using so many Sass variables](http://bensmithett.com/stop-using-so-many-sass-variables/)   

[Gist](http://sassmeister.com/gist/7f5629c1214dea4cee75)

### #4 Extend
CSS rules reuse and inheritance.    
1. [Understanding placeholder selectors](http://thesassway.com/intermediate/understanding-placeholder-selectors)   

[Slider](http://slides.com/ganlanyuan/deck-1#/)   
[Gist](http://sassmeister.com/gist/d93b750bbc9641b5d382) 


**@extend**  
````scss
.class {
  // Css properties;
}
#id {
  // Css properties;
}
%selector-placeholder {
  // Css properties;
}
.header {
  @extend .class;                 // use extention
  @extend #id;                    // use extention
  @extend %selector-placeholder;  // use extention
}
````  

### #5 Function & Mixin
Writing reusable styles mixed.   
1. [Sass: Mixin or Placeholder?](http://www.sitepoint.com/sass-mixin-placeholder/)   
2. [Creating a Repeatable Style Pattern with Sass: Placeholders vs. Mixins](http://jdsteinbach.com/css/sass/creating-repeatable-style-pattern-sass-placeholders-vs-mixins/)   
3. [REM to PX Browser Function with Sass](http://davidwalsh.name/rem-px-browser-function-sass)   

[Slider](http://slides.com/ganlanyuan/deck-1-2#/)   
[Gist-function](http://sassmeister.com/gist/6aa491d689e90ae63bbb)   
[Gist-mixin](http://sassmeister.com/gist/b936f16cf1af9759411f)  

**@function** 
````scss
@function em($val) {
  // Do something;
}
width: em(10px);        // use function
````

**@mixin**  
````scss
@mixin name($val) {
  // Do something;
}
.header {
  @include name(10px);  // use mixin
}
````

### #6 Directive
@if, @for, @each and @while.    
1. [Sass control directives: @if, @for, @each and @while](http://thesassway.com/intermediate/if-for-each-while)   

**@if**    
````scss
@if conditions {
  // statements;
} 
@if conditions {} @else {}              // if ... else ...
@if conditions {} @else if {} @else {}  // if ... else if ...
````

**@for**
````scss
@for $i from 1 to 10 {        // to: not include 10
  // statements;
}
@for $i from 1 through 10 {   // through: include 10
  // statements;
}
````

**@each**
````scss
@each $item in $items {
  // statements;
}
````

**@while**
````scss
@while conditions {
  // statements;
}
````

### #7 List & Map
Use list and map to write efficient style sheet.  
1. [Understanding Sass lists](http://hugogiraudel.com/2013/07/15/understanding-sass-lists/)   
2. [Advanced Sass list functions](http://hugogiraudel.com/2013/08/08/advanced-sass-list-functions/)    
3. [Using Sass Maps](http://www.sitepoint.com/using-sass-maps/)
4. [Take your Sass skills to the next level with list-maps](https://www.codefellows.org/blog/so-you-want-to-play-with-list-maps) 

**list** 
````scss
$list: ();                                            // initalize
$list-a: 'value-1' 'value-2' 'value-3' 'value-4';     // separator: ' '
$list-b: 'value-1', 'value-2', 'value-3', 'value-4';  // separator: ','
$list-b: (
  'value-1', 
  'value-2', 
  ('value-3.1', 'value-3.2', 'value-3.3', 'value-3.4'), 
  'value-4'
  );            // nested list
nth($list, 1)   // get value (indexes start at 1, not 0)
length($list)   // get length
````
**map**
````scss
$map: ( key:value, key-2:value-2, key-3:value-3 );  // initalize
map-has-key($map, key)                              // check if the map has the key
map-get($map, key)                                  // get the value
map-get-z($map, key, key, ...)                      // get the value
````

### #8 Color
Color functions and management.   
1. [Managing relationships between colours with Sass](http://maketea.co.uk/2014/07/21/managing-relationships-between-colours-with-sass.html)   

### #9 Write your components
Basis rules to write your components.   

### #10 Rocket usage
Learn to use Rocket.   
