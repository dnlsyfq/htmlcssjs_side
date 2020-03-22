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
* transform: scale(int); /*change the scale of an element*/

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

* width: px | em | % ;
* height: px| em | % ;
* background-color: rgba(digit,digit,digit,0-1) 0 clear 1 opaque
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