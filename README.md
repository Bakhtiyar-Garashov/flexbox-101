# A guide contains everything you know about CSS flexbox

### Table of Contents

#### 1. Introduction

>The Flexible Box Module, usually referred to as flexbox, was designed as a one-dimensional layout model, and as a method that could offer space distribution between items in an interface and powerful alignment capabilities. This article gives an outline of the main features of flexbox, which we will be exploring in more detail in the rest of these guides.

>When we describe flexbox as being one dimensional we are describing the fact that flexbox deals with layout in one dimension at a time — either as a row or as a column. This can be contrasted with the two-dimensional model of CSS Grid Layout, which controls columns and rows together.

During the good old days of the Web float and table were heavily used.

<cite>[MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) <cite>

**Flex container** - A parent element that establishes a flex container by defining CSS ```display: flex; ``` attribute.

**Flex items** - Elements that are children of a flex container.

Let's look at very basic example:

```html 
<div class='parent'>
    <div class='child'></div>
    <div class='child'></div>
    <div class='child'></div>
    <div class='child'></div>
    <div class='child'></div>
</div>
```
```css
.parent {
  display: flex;
  flex-direction: column;
}

.child {
  height: 30px;
  margin: 10px 0;
  width: 100%;
  border: 1px solid black;
}
```
In the example above div element with the name parent defines the flex container and contains 5 children div elements.

Another important concept of CSS flex model is axes which defines the alignment of children in the flex container whether vertical or horizontal. When working with flexbox you need to think in terms of two axes — the main axis and the cross axis. The main axis is defined by the flex-direction property, and the cross axis runs perpendicular to it. Everything we do with flexbox refers back to these axes, so it is worth understanding how they work from the outset. Probably you are gonna need only to define main axis not the cross one.

The main axis is defined by ```flex-direction```, which has four possible values:

- row
- row-reverse
- column
- column-reverse

![Row](images/axis1.png)

Choose ```column``` or ```column-reverse``` and your main axis will run from the top of the page to the bottom — in the block direction.

![Column](images/axis2.png)
