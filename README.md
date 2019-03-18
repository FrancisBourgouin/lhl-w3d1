# Lecture W3D1

## Content

- New Project: Tweeter
- Role of HTML, CSS, JavaScript
- HTML
  - Structure of HTML documents
  - Structure of tags
  - Semantic HTML
- Cascading Style Sheets
  - How to define styles
- The CSS Box Model
  - inline, block, inline-blocks
  - Properties of the box model (padding, etc)
  - Box-sizing

## Roles

- HTML: Structure of the document
- CSS: Document styling
- JavaScript: Interactivity

## HTML

- Hypertext Markup Language

### Structure of the document

- 2 parts: head and body

- Doctype and language

- Doctype declares the version specification of HTML (HTML 5 in this case)
- lang attribute helps the browser figure out the language of the page

```
<!DOCTYPE html>
<html lang="en">
...
```

```
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>My Title</title>
</head>
```

- charset: specifies the character encoding
- viewport: adapt the page for mobile in terms of width and zoom level
- X-UA-Compatible: what version of Internet Explorer the page should be rendered as

```
<body>

<p>Your content goes in between the body tags.</p>

</body>
</html>
```

### Structure of tags

- Markup of tags opening and closing:

`<p>This text goes in between the opening and closing tags</p>`

- Self-closing tags

`<img src="image.png">`

- tags with attributes

`<input type="text" id="name" name="name" placeholder="Entrez votre nom">`

### Semantic HTML

- Historically we used the div tag to structure sections of the content
- The div is a general purpose tag with no meaning
- Instead of using regular div, we'll use semantic tags

  - header
  - nav
  - main
  - article
  - aside
  - footer
  - section

  [Semantic HTML](https://internetingishard.com/html-and-css/semantic-html/)

## CSS

- Cascading Style Sheets

### How to define styles

```
selector {
  property: value;
  property: value;
  property: value;
}
```

- `selector` will target elements on the page that the style gets applied`
- `property` is the css property that needs to be modified

- When you inspect an element in DevTools, you can set the values directly and play around

[MDN CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

### Adding styles to our page

- 3 ways:

1. Inline
2. Internal
3. External

### Libraries/CSS Framework

- Reset / normalize
- Bootstrap
- Google Fonts

- Resetting all the default styles of the browsers to reduce inconsistencies

[Normalize CSS](https://necolas.github.io/normalize.css/)

### The Box model

- CSS uses boxes around each HTML of a web page to define its layout

[Let's have a look at the New York Times](https://www.nytimes.com/)

- Using the [Web Developer extension](https://chrispederick.com/work/web-developer/), we can see the boxes around the elements of the page.

- We have different types of boxes

  - block-level elements
  - inline-block level elements

#### Block-Level Elements

[Example](./blocks.html)

- Key characteristics of block elements

  - They take the full width of the horizontal space available defined by its parent container
  - Each element will occupy a row
  - Multiple block-level elements will stack on each other
  - You can set CSS box properties to change their appearance
  - Block-level elements rely on the box model

#### Inline-Block Elements

- Inline block allow inline elements to behave like block elements

#### Box Model

- We can easily see the box model in Chrome DevTools
- The box model relies on these properties

  - Content – Content of the element.
  - Padding – The space between the box’s content and its border.
  - Border – The line between the box’s padding and margin.
  - Margin – The space between the box and surrounding boxes.

- Padding, border, and margin can be changed with CSS

```
  h1 {
    padding: 0.5em;
    border:royalblue 1px solid;
    margin: 0;
  }

  p {
    padding: 0.5em;
    margin: 0.2em 0;
    border:royalblue 1px solid;
  }
```

##### Problems with the default box model

- The width property refers to the width of the content. Width of the borders and padding need to be added to know the final size

- Solution: set the `box-sizing` property to `border-box`

### CSS Layout

- In terms of layout, back in the days, we use to position elements with html tables!

- Today, we have a few options:

  - Floats
  - Absolute positioning
  - Flexbox
  - Flexgrid

### Floating Elements

- Using Float is a hack and never was intended for CSS layout
- A floated element is taken out of the normal document flow
- Float need to be cleared with a hack

```
.clearfix::after {
  display: table;
  content: "";
  clear: both;
}
```

### CSS Positioning

- Position relative

  - Set the element as the parent
  - Relative makes the element part of the normal document flow

- Position absolute

  - Use a x,y position relative to the parent that is set to relative to positiom the element

- Position fixed

  - Position an element relative to the document window. Remains fixed at an x,y position
  - Z-index property sets the stacking order

### Flexbox

- Flexbox is a grid-based layout
- With Flebox items are directed, aligned, ordered, and flexible
- Flexbox items are designed to best fill the space of their container
- Some of the problems solved with Flexbox are: simpler grid systems, a and hack-free layout system

[CSS Tricks - Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## References

[Semantic HTML](https://internetingishard.com/html-and-css/semantic-html/)
CSS-tricks - good resource for hands-on CSS tutorials: https://css-tricks.com

[Normalize CSS](https://necolas.github.io/normalize.css/)
