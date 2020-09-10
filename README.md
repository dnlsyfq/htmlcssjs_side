# HTML

**Attributes**

* input type
```
<input type="email" name="email_address" required>

<input type="email" name="email_address" required="">
```

**Markdown**

* less than , < 
```
&lt;
```

* greater than, >
```
&gt;
```

* ampersand, &
```
&amp;
```
<p>Everyone loves fonts by Ambercrombie &amp; Fitch </p>

(ASCII)[http://www.ascii.cl/htmlcodes.html]

**Html Language**
* follow ISO 639-2
* [other language codes](http://www.loc.gov/standards/iso639-2/php/code_list.php)

```
<html lang="en">
</html>
```

# CSS

---
**Text**

* text-align : justify | center | right left ;
* font-weight:bold | int only;
* text-decoration:underline;
* font-style: italic;
* text-decoration: line-through;
* font-size:23;
* text-transform:lowercase|uppercase|capitalize|initial|inherit|none;
* transform: scale(int)|skewX(deg)|skewY(deg); /*change the scale of an element*/

|value|result|
|---|---|
|initial|Use the default value|
|inherit|Use the text-transform value from the parent element|
|none|Default: Use the original text|

* line-height:25px; /*changes the amount of vertical space that each line of text gets.*/
* pseudo class , pseudo-class is a keyword that can be added to selectors, in order to select a specific state of the element.

* pseudo class 
anchor tag hover state ,  styling of an anchor tag can be changed for its hover state using the :hover pseudo-class selector.
```
<style>
  a {
    color: #000;
  }

  a:hover{
    color:blue;
  }

</style>
<a href="http://freecatphotoapp.com/" target="_blank">CatPhotoApp</a>
```
* position: relative | absolute | fixed;

```
<style>
  h2 {  
    position:relative;
    top:15px;
  }
</style>
```

```
p:hover {
  transform: scale(2.1);
}

<style>
  div {
    width: 70%;
    height: 100px;
    margin:  50px auto;
    background: linear-gradient(
      53deg,
      #ccfffc,
      #ffcccf
    );

    div:hover{
      transform:scale(1.1);
    }
  }



</style>

<div></div>
```

* pseudo elements , ::before , ::after

 These pseudo-elements are used to add something before or after a selected element. In the following example, a ::before pseudo-element is used to add a rectangle to an element with the class heart

 ```
<style>
  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: rotate(-45deg);
  }
  .heart::after {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart::before {
    content: "";
    background-color: pink;
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }
</style>
<div class="heart"></div>

 ```


---
**Navigation Bar**

```
  #navbar {
    position:fixed;
    top:0px;
    left:0px;
    width: 100%;
    background-color: #767676;
  }
    <nav id="navbar">
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Contact</a></li>
      </ul>
    </nav>
```


---
**Image**

```
<figure>
  <img src="imgs/Ashtabula.jpg" width="500px|50%" alt="My house">
  <figcaption>Set image size</figcaption>
</figure>
```

* PNG in WEB
```
<link rel='icon' type="image/png" href="./_.png">
```

* width: px | em | % ;
* height: px| em | % ;
* background-color: transparent| rgba(digit,digit,digit,0-1); 0 clear 1 opaque
* opacity: 0-1;
* z-index: digit; /*z-index property can specify the order of how elements are stacked on top of one another. */
* margin: auto; /**/
```
rgba stands for:
  r = red
  g = green
  b = blue
  a = alpha/level of opacity
```

* box-shadow applies one or more shadows to an element.
> offset-x (how far to push the shadow horizontally from the element),
> offset-y (how far to push the shadow vertically from the element)
> box-shadow: offset-x offset-y blur-radius spread-radius color;

```
box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
```
---



**Color**

* color transitions

background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);

```
background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));


  div {
    background: repeating-linear-gradient(
      45deg,
      yellow 0px,
      yellow 40px,
      black 40px,
      black 80px
    );
  }

  <div></div>
```

```
<style>
  body {
    background:url(https://cdn-media-1.freecodecamp.org/imgr/MJAkxbh.png);
  }
</style>
```
---

**Animation properties**

* @keyframes

To animate an element, you need to know about the animation properties and the @keyframes rule. The animation properties control how the animation should behave and the @keyframes rule controls what happens during that animation. There are eight animation properties in total. 

* animation-name sets the name of the animation, which is later used by @keyframes to tell CSS which rules go with which animations.

* animation-duration sets the length of time for the animation.


@keyframes is how to specify exactly what happens within the animation over the duration. This is done by giving CSS properties for specific "frames" during the animation, with percentages ranging from 0% to 100%. If you compare this to a movie, the CSS properties for 0% is how the element displays in the opening scene. The CSS properties for 100% is how the element appears at the end, right before the credits roll. Then CSS applies the magic to transition the element over the given duration to act out the scene.


```
#anim {
  animation-name: colorful;
  animation-duration: 3s;
}

@keyframes colorful {
  0% {
    background-color: blue;
  }
  100% {
    background-color: yellow;
  }
}
```

* @keyframes with hover state

```
<style>
  img:hover {
    animation-name: width;
    animation-duration: 500ms;
  }

  @keyframes width {
    100% {
      width: 40px;
    }
  }
</style>

<img src="https://bit.ly/smallgooglelogo" alt="Google's Logo" />
```


Note that ms stands for milliseconds, where 1000ms is equal to 1s.
```
<style>
  button {
    border-radius: 5px;
    color: white;
    background-color: #0F5897;
    padding: 5px 10px 8px 10px;
  }

  button:hover {
    animation-name: background-color;
    animation-duration: 500ms;
  }

  @keyframes background-color{
    100%{     background-color:#4791d0;
    }
  }

</style>

<button>Register</button>
```

animation resets after 500ms has passed, causing the button to revert back to the original color. You want the button to stay highlighted.

This can be done by setting the animation-fill-mode property to forwards. The animation-fill-mode specifies the style applied to an element when the animation has finished. You can set it like so:

animation-fill-mode: forwards;

```
<style>
  button {
    border-radius: 5px;
    color: white;
    background-color: #0F5897;
    padding: 5px 10px 8px 10px;
  }
  button:hover {
    animation-name: background-color;
    animation-duration: 500ms;
    /* Only change code below this line */
    animation-fill-mode:forwards;
    /* Only change code above this line */
  }
  @keyframes background-color {
    100% {
      background-color: #4791d0;
    }
  }
</style>
<button>Register</button>
```

* Movement Using CSS Animation

When elements have a specified position, such as fixed or relative, the CSS offset properties right, left, top, and bottom can be used in animation rules to create movement.

```
@keyframes rainbow {
  0% {
    background-color: blue;
    top: 0px;
  }
  50% {
    background-color: green;
    top: 50px;
  }
  100% {
    background-color: yellow;
    top: 0px;
  }
}
```
```
<style>
  div {
    height: 40px;
    width: 70%;
    background: black;
    margin: 50px auto;
    border-radius: 5px;
    position: relative;
  }

  #rect {
    animation-name: rainbow;
    animation-duration: 4s;
  }

  @keyframes rainbow {
    0% {
      background-color: blue;
      top: 0px;
      left: 0px;

    }
    50% {
      background-color: green;
      top: 50px;
      left:25px;

    }
    100% {
      background-color: yellow;
      top: 0px;
      left:-25px;
    }
  }
</style>

<div id="rect"></div>

```

to control how many times you would like to loop through the animation. Here's an example:

> animation-iteration-count: 3;

In this case the animation will stop after running 3 times, but it's possible to make the animation run continuously by setting that value to infinite.

```
<style>
  .back {
    position: fixed;
    padding: 0;
    margin: 0;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: white;
    animation-name: backdiv;
    animation-duration: 1s;
    animation-iteration-count:infinite;
  }

  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: rotate(-45deg);
    animation-name: beat;
    animation-duration: 1s;
    animation-iteration-count:infinite;
  }
  .heart:after {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart:before {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }

  @keyframes backdiv {
    50% {
      background: #ffe6f2;
    }
  }

  @keyframes beat {
    0% {
      transform: scale(1) rotate(-45deg);
    }
    50% {
      transform: scale(0.6) rotate(-45deg);
    }
  }

</style>
<div class="back"></div>
<div class="heart"></div>

```

* animation-timing-function says how the car accelerates and decelerates over the course of the drive.
```
animation-timing-function: ease|ease-out|ease-in|linear;
animation-timing-function: cubic-bezier(0.25, 0.25, 0.75, 0.75);
```
---

# Drop Down





# CSS3

* hsl()

**Hue**

Hue is what people generally think of as 'color'. If you picture a spectrum of colors starting with red on the left, moving through green in the middle, and blue on right, the hue is where a color fits along this line . angle of the color on the circle is given as a value between 0 and 360.

**Saturation**

 amount of gray in a color. A fully saturated color has no gray in it, and a minimally saturated color is almost completely gray. This is given as a percentage with 100% being fully saturated.

 **Lightness**

the amount of white or black in a color. A percentage is given ranging from 0% (black) to 100% (white), where 50% is the normal color.

```
 .green {
    background-color: hsl(120, 100%, 50%);
  }

```

# HTML

* bold 
```
<strong></strong>
```

* underline
```
<u></u>
```

* italic
```
<em><em>
```
* strikethrough
```
<s></s>
```

* horizontal line 
```
<hr>
```

* hyperlink

target 
```
 _self
 _blank
 _top
 _parent
 ```


 * Audio , Video 

 <video src="_.mov" width="400" controls></video>

 <audio src="_.ogg#t=15:35" controls></audio>

 * Table

 ```
 <table border=1>
 <tr><th></th></tr>
  <tr><td rowspan=2></td></tr>
 </table>
 ```

 * Tags

 **Generic**
  * <p>, <div>

**Semantic**
  * <header>, <nav>, <footer>, <figure>

* Block Tags
  * Containers : <article>, <aside>, <section>, <main>
  * <hr>
  * <address>
  * <blockquote> 
  * details
---

# NPM 

```
npm install --save @fortawesome/fontawesome-free

https://github.com/FortAwesome/Font-Awesome

```