# html-css

This repository contains comprehensive notes on HTML and CSS. It's designed as a reference for front-end development concepts and techniques, including basic to advanced topics. Perfect for students, self-learners, and developers looking to refresh their knowledge or learn new tricks in HTML and CSS.

---

![image1](https://github.com/melodiaz23/html-css/blob/master/images/Pasted%20image%2020231217160457.png?raw=true)

- Whenever the files that make up the website are simply stored on the web server and are then sent to the browser as they are, we say that we have a static website.

- So, a **static website** es basically a website where the files are simply sent from the server to the browser as they are.

- We say that we have a **dynamic website** when the website is dynamically assembled from different pieces on the server.

![[https://github.com/melodiaz23/html-css/blob/master/images/Pasted%20image%2020231217163123.png?raw=true]]

# HTML

> HyperText Markup Language - Is a markup language, use to structure and describe the content. - Consists of elements: - paragraphs - links - headings - images - videos

![[Pasted image 20231217194429.png]]

## HTML document structure

```html
<!DOCTYPE html>
<!-- 1. -->
<html lang="en">
  <!-- 2. -->
  <head>
    <!-- 3. -->
    <meta charset="UTF-8" />
    <meta
      http-equiv="X-UA-Compatible"
      content="IE=edge" />
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
  <!-- 4. -->
</html>
```

> Every HTML document always needs to star with HTML element (2.), and inside of it we need one head element (3.) and one body element (4.).

- Every HTML document needs to start with the doctype. This let the browser know that we are using HTML.
- The head element are for things that are not visible in the browser window. Inside of it we have:
  - title
- The body is for all the elements that will be visible on the page.

> [!NOTE]
> We always need to have an HTML element with a head and with a body. What we put in there is optional but head and body are not optional.

## Text Elements

### Headings

> The goal of headings is to break up big blocks of text into more logical sections, and to basically add a title to each of these sections.

We can establish a hierarchy in our text:

```html
<h1>The Basic Language of the Web: HTML</h1>
<!-- Every page should only have one H1 heading -->
<h2>The Basic Language of the Web: HTML</h2>
<h3>The Basic Language of the Web: HTML</h3>
<h4>The Basic Language of the Web: HTML</h4>
<h5>The Basic Language of the Web: HTML</h5>
<h6>The Basic Language of the Web: HTML</h6>
```

![[Pasted image 20231217201428.png]]

### Paragraph

> Generic element that we use to mark up bigger blocks of text.

```html
<p>Posted by <strong>Laura Jones</strong> on Monday, <em>June 21st 2027<em></p>
```

> Use `<b></b>` and `<i></i>`is not a good practice. We use `<strong></strong>` and `<em></em>`.

### Lists

```html
<ol>
  <!-- Parent element -->
  <li>The opening tag</li>
  <!-- Child element -->
  <li>The closing tag</li>
  <li>The actual element</li>
</ol>
```

> `ol` for ordered list and `li` for list items.
> The container of another elements is the parent and the elements that are inside the parent are the child elements.

```html
<ul>
  <li>To be able to use the fundamental web dev language</li>
  <li>To build web applications</li>
  <li>To impress friends</li>
  <li>To have fun 😃</li>
</ul>
```

> `ul` stands for unordered list

### Html entity

We find it with `&`and after that the option we want to add:

```html
Copyright &copy;
```

> Copyright ©

Resources: https://css-tricks.com/snippets/html/glyphs/

## Images and attributes

The image element is a special kind of element. Since It doesn't have content, It doesn't have a closing tack.

```html
<img />
```

**Attributes** are basically pieces of data which we can use to describe elements. One of this attributes are:

- `src=""` --> Here we can specify the source of the image.
- `alt=""` --> We should never skip. We need to specify here, some text that should describe what the image is about.
- `width=""` and `height=""` --> The size of the image

We can also specify attributes in some other elements:

- HTML Element:
  - `lang="en"` --> Language

* `<meta />` --> meta stand for metadata:
  - `charset="UTF-8"` --> The character set should be UTF-8, which basically is all the simple characters that we use in the English language.

## Hiperlinks

We have 2 categories:

- Links that point to other pages within our own website.

```Html
<a href="blog.html">Blog</a>
<a href="#">Challanges</a> <!-- Don't go to anywhwere, is like a placeholder link -->
```

> What makes and anchor element really a link is the `href` property.

- Links that point to outside of our website.

```html
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML">MDN Web Docs</a>
```

- `href=""` --> We put the url of the page we are going to link.
- `target="_blank"` --> The page open into a new tab.

## Semantic HTML

> What this means is that certain elements have actually a meaning or a purpose attached to them.

- `<nav></nav>` --> Navigation.
- `<header></header>` --> Header: Introduction for the website
- `<article></article>` --> Article
- `<footer></footer>` --> Foot of the page
- `<aside></aside>` --> Use for secondary information that complements the information in the main part of the page (usually use as a sidebar).
- `<div></div>` --> We use it when we don't want to attach a certain meaning to a certain container.

This elements doesn't do anything by its own, just group the elements, but we do it this way (different names) for the semantic HTML and also for stying with CSS.

# CSS

> Cascading Style Sheets
>  - Describes the visual style and presentation of the content written in HTML
>  - Consist of properties:
>  - font
>  - text
>  - spacing
>  - layout

![[Pasted image 20231218205556.png]]

> The CSS file is always composed of multiple CSS rules.

## Inline, Internal and External CSS

**Inlice CSS**

> Writing the CSS code inside of the element. Should usually never be used.

```html
<h1 style="color: rgb(73, 73, 156)">📘 The Code Magazine</h1>
```

**Internal CSS**

> We go to the head and declare the style element. Not practical if we have a lot of CSS Code

```html
<head>
  <style>
    h1 {
      color: rgb(63, 63, 196);
    }
  </style>
</head>
```

**External CSS**

> Putting all the CSS code into a special CSS file.

```html
<head>
  <link
    rel="stylesheet"
    href="style.css" />
</head>
```

> `<link>` element has the purpose to connect the HTML file to a CSS file.

```css
h1 {
  color: blue;
}
```

## Styling text

```css
h1 {
  font-size: 20px;
  font-family: sans-serif;
  text-transform: uppercase;
  font-style: italic;
}

h2 {
  font-size: 40px;
  font-family: sans-serif;
}

h3 {
  font-size: 30px;
  font-family: sans-serif;
}

h4 {
  font-size: 20px;
  font-family: sans-serif;
  text-transform: uppercase;
  text-align: center; /* In the center of the parent element */
}

p {
  font-size: 22px;
  font-family: sans-serif;
  line-height: 1.5; /* The line height will be 1.5 times the font size */
}

li {
  font-size: 20 px; /* 16 px by default */
  font-family: sans-serif;
}
```

### Combining Selectors

We can create a list of selectors:

```css
h1,
h2,
h3,
h4,
p,
li {
  font-family: sans-serif;
}
```

We use a descendent selector:

````css
footer p {
  font-size: 16px;
}

article header p {
  font-style: italic;
}```
> It will select all the p elements that are inside of footer elements. But this is not a good idea, since encodes the HTML structure.

Or we can give name to some elements (`id="name"`)and them selected:

```html
 <p id="author">Posted by <strong>Laura Jones</strong> on Monday, June 21st 2027</p>
````

> We are not allowed to repeat id names.

```css
#author {
  font-style: italic;
}
```

> In our CSS, we can use the id # selector

Besides id theres another way of giving elements names, using class:

```html
<p class="related-author">By Jonas Schmedtmann</p>
```

```css
.related-author {
  font-size: 18px;
  font-weight: bold;
}
```

> For classes we use the class (`.`) selector

## Colors

![[Pasted image 20231219105421.png]]

![[Pasted image 20231219105844.png]]

```css
aside {
  background-color: #f7f7f7;
  border: 5px solid #1098ad; /* here we define: border width, border style, border color */
}

body {
  background-color: #f7f7f7;
}
```

## Pseudo-Classes

```css
li:first-child {
  font-weight: bold;
}
li:last-child {
  font-style: italic;
}
li:nth-child(2) {
  /* We need to specify the number child or use keywords (like odd)*/
  color: red;
}
article p:last-child {
  /* It only works if the p element is the last child*/
  color: red;
}
```

> first-child is the seudo-class. It will select all the li elements that are the first-child elements of its parent elements.

### Style Hiperlinks

```css
/* To style all the anchor element with href attribute */
a:link {
  color: #1098ad;
  text-decoration: none;
}

a:visited {
  color: #1098ad;
}

a:hover {
  color: #444;
  font-weight: bold;
  text-decoration: underline wavy orangered;
  /* text-decoration we define text-decoration line, style and color */
}

/* The state in we are actually clicking */
a:active {
  background-color: black;
  font-style: italic;
}
```

> This forth states are always define in this exact order.

## Properties

### Font

- font-family: sans-serif;
- font-size: 18px;
- font-style: italic;
- font-weight: bold;

### Text

- text-transform: uppercase
- text-decoration: none; ---> underline
- line-height: 1.4;

### List

- list-style: none;

### Color

- color: `#fff`
- background-color: `#f7f7f7`;
- border: 5px solid `#1098ad`;
  - border-top: 5px solid `#1098ad`;
  - border-bottom: 5px solid `#1098ad`;
  - border-left: 5px solid `#1098ad`;
  - border-right: 5px solid `#1098ad`;

### Link

- cursor: pointer;

### Box Model

- margin: 0;
  - margin-bottom: 60px;

* padding: 0;
  - padding-left: 40px;
  - padding-right: 40px;
  - padding: 20px 40px;
* width: 500px;
* height: 80px;

## CSS Fundamentals

### Theory #1: Conflicts between selectors

![[Pasted image 20231219133613.png]]

![[Pasted image 20231219133632.png]]

> `*` Universal selector allow apply a certain style to every single element on the page.

> [!NOTE]
> If one selector is way more complex than the other, then many times it's actually the more complex one that gets applied.
> **Is better keep our selector simple.**

### Theory #2: Inheritance and the universal selector

Inheritance is a mechanism by which some styles, so some properties get their values inherited from parent elements to child elements.

![[Pasted image 20231219152948.png]]

### Theory # 3: The CSS Box Model

The box model defines how elements are displayed on a webpage and how they are sized. So in this box model, each and every element on a webpage can be seen as a rectangular box, and each of these boxes can have content, a border, and space inside and outside of it.

![[Pasted image 20231219164904.png]]

![[Pasted image 20231219165632.png]]

```css
* {
  /* Global selector to reset margin and padding */
  margin: 0;
  padding: 0;
}

.main-header {
  background-color: #d2cccc;
  /* padding: 20px;
  padding-left: 40px;
  padding-right: 40px; */
  /* TOP - BOTTOM and righ and left */
  padding: 20px 40px;
}
```

#### Collapsing margins

When we have two margins that occupy the same space, only one of them is actually visible on the page. And that is usually the larger of the two.

> [!NOTE]
> Whenever you need some space inside of an element, then you always use padding. On the other hand, in order to create space outside of an element, or also to create space between multiple elements, always use margin.
>
> And in case that you need to add vertical space, then I advise you to most of the time stick to margin and bottom.

```css
.post-image {
  /* width: 800px; */
  width: 100%;
  height: auto;
}
```

> Specifying the height and setting it to auto is only necessary if that height is already specified before in HTML. So in case we don't specify any image dimensions in HTML, then if we set the height or the width using CSS, the other one will automatically adapt in order to account for the original aspect ratio of the image.
>
> - The percentage is usually the percentage of the width of the parent container.

```css
.container {
  width: 700px;
  margin: 0 auto;
  /* Auto stands for automatic and means margin at the left must be the same as the right */
}
```

### Theory 4: Types of Boxes

#### Block level elements

![[Pasted image 20231219210945.png]]

#### Inline elements

![[Pasted image 20231220085644.png]]

> [!important]
> We usually don't set the height to a specific value, because the element did not expand in order to fit the content.

- In so many situations we transform a block level element into something called an inline block element.

![[Pasted image 20231220153400.png]]

### Theory # 5: Absolute positioning

![[Pasted image 20231220155130.png]]

![[Pasted image 20231220160117.png]]

Example:

```html
<button class="like">Like ❤️</button>
```

```css
body {
  position: relative; (1)
}

.like {
  font-size: 22px;
  padding: 20px;
  cursor: pointer;
  position: absolute;
  /* By defult this position is set in relation to the viewport*/
  /* bottom: 0;
  left: 0; */
  bottom: 50px;
  right: 50px;
}

```

> We need specific set the position of that parent element to relative.

## Pseudo-elements

> Pseudo-elements are elements that don't exist in the HTML but that we can still select and style in CSS.

> [!NOTE]
> Pseudo classes are written with just one colon, and the pseudo-elements are with two colons.

```css
h1::first-letter {
  font-style: normal;
  margin-right: 5px;
}

h1::first-line {
  font-style: normal;
  margin-right: 5px;
}
```

- Siblings elements are when both elements share the same parent. Adjacent sibling is the very next element (that comes after the element)

```css
h3 + p::first-line {
  color: red;
}
```

> The plus `+` is the adjacent sibling selector.

### Before and after pseudo-elements

```css
/* h2::before */
h2::after {
  /* content property is needed, could be empty string */
  content: 'TOP';
  background-color: #ffe70e;
  color: #000;
  font-size: 16px;
  font-weight: bold;
  display: inline-block;
  padding: 5px 10px;
  position: absolute;
  right: -10px;
  top: -25px;
}
```

> CSS, once we declare it here, will then automatically create it, and will put it here so that we can style it.

`after` will basically become the very last child element of the one that we are selecting, while `before` will become the very first child element.

# Building Layouts

Layout is the way text, images and other content is placed and arranged on a webpage.

So, building a layout means to arrange page elements into a visual structure, instead of simply having them placed one after another (normal flow)

There are 2 types of layouts:

![[Pasted image 20231228151156.png]]

![[Pasted image 20231228152407.png]]

## Floats Layouts

> When an element is floated, it is removed out of the normal flow.

```HTML
  <img
	src="img/laura-jones.jpg"
	alt="photo of laura jones"
	width="50"
	height="50" class="author-img"/>
  <p id="author" class="author">
	Posted by <strong>Laura Jones</strong> on Monday, June 21st 2027
  </p>
```

```CSS
.author-img{
  float: left;
}
```

> The image is basically going to be taken out of the document flow just like an absolutely positioned element. The difference with floats is that all the other elements will basically float around it.

```css
.author {
  /* padding-left: 80px; */
  float: left;
  margin-top: 10px;
  margin-left: 20px;
}
```

> We have to also make the other element, float. This could be done in a modern way, though.
>
> - Floated element is still able to create some margins around it.

```css
h1 {
  float: left;
}

nav {
  float: right;
}
```

> With float is like the elements doesn't exist. This cause a phenomena call the collapsing element. This did happen because both of its children are now floated.

![[Pasted image 20231228211225.png]]

### Clearing floats

- One way (bad practice):

1. Create a div element inside the container and clear the floats.

```html
<div class="clear"></div>
```

2. In the CSS file, selecting the element, use the clear property.

```css
.clear {
  clear: both;
}
```

> Or clear right or left if we want to clear one side or another.

Another way:

1. On the element we has the collapsed heigh, we add a class usually call "clearfix"
2. And on the CSS: tra

```css
.clearfix::after {
  clear: both;
  content: '';
  display: block;
  /* Only works on block level element */
}
```

> This was call "clearfix hack". Is not use anymore.

> [!Useful]
> If the width of the container is 1200px, we can divide it into the elements inside of it, like 900px-300px for example.

## Flexbox

![[Pasted image 20240425201123.png]]

> [!NOTE]
> A flex container is also something like a block element.

>

## CSS Grid

![[Pasted image 20240425201043.png]]

# Components and layout patterns

# Useful pages

- https://css-tricks.com/snippets/html/glyphs/
- HTML validator: https://validator.w3.org/
- diffchecker: https://www.diffchecker.com/

# Resources

#Resources

- https://loading.io/css/

* https://css-tricks.com/snippets/css/complete-guide-grid/#aa-introduction
