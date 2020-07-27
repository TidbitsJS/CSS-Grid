# CSS Grid : Let's GriddYup

![CSS Grid](./Images/cssGrid.png)

A CSS tool to create two-dimensional layouts on the web

## Introduction

A 26 video pack of WESBOS covers all the fundamental & advanced properties of CSS Grid that you need to learn. While learning Grid, I have decided to create a tutorial in my own language for self betterment & for others if it helps them in any way. Below are my wordings ready to take you on an adventure!

To get started, firstly create some starter files in your system to get along on the journey. You need to create a style page which will be used throughout the course. A `style.css` file has been created in the root folder.

`Image` folder contains the needed images that are required in this course for explanation & other things.

### 1.1 Grid Fundamental

Create a html file & don't forget to link `style.css` file.

As you can see my html file in `Grid Fundamentals`, it contains a `div` element with class `container` like below.

```html
<div class="container">
  <div class="item">Item</div>
</div>
```
Note: You can add as much of `item` you want in your `container`.

If you haven't observed `style.css` properly then you all will be wondering about why children of container contain the same class name i.e `item`.

Let's study it in bit. You can see the style definition for `item` in the file. Ahh there it is, that you are looking, `display: grid` thing. That's what we all are here to learn about, GriddYup !

To use the CSS Grid tool, you have to first declare the display as grid like all other, know what I mean by 'all other'? These include our flexbox, block, inline, inline-block, or none. If you have ever used `flexbox`, then you might be aware of `justify-content` & `align-items`, right? If you are not, then these are the properties we can use to align or structure items respectively of their value. Here, it's the center.

```css
.item {
  display: grid;
  justify-content: center;
  align-items: center;
  border: 5px solid rgba(0, 0, 0, 0.03);
  border-radius: 3px;
  font-size: 35px;
  background-color: var(--yellow);
}
```

Now you are comfortable with container & it's children, We can head forward to get our hands on our first tutorial i.e. Gird Fundamentals. Here we are displaying the container as Grid. Wait, what do you mean by displaying a grid? Before knowing about the grid, first let's clear this field of display. Display is kinda behaviour to render the box, that is how you want to see it as in your page. What as? Yeah the element to whom you are using this display properly. Cool!

What do you think of Grid? Yeah you got this. Its a structure of rows & columns. You Genius! Let's not delay further. Jump right on the properties of grid.

You see grid as a structure of rows & columns. But how you define these stuffs. If you want five columns for your beautiful photo gallery, how do you do that using grid? Great question! This is where `grid-template-columns` comes handy. You want columns, use that property with your choice of column size. There is no rule that all columns should have the same size. Not at all. Do anything you want bud.   

```css
.container {
  display: grid;
  grid-template-columns: 100px 200px auto;
  grid-template-rows: 100px 150px;
  grid-gap: 20px;
}
```

Auto? What's that little word doing in `grid-template-columns`? Here for you, an explanation. Suppose, You want two to three columns of your choice of size and for the next column you don't want a fixed size. You instead want that to take the remaining place on your page. So far with me? Yeah it means it will adjust accordingly the size of the web page. Super flexible!

Happy with columns, now what about rows? So smart han? Yeah you are right, use `grid-template-rows` for declaration of how many rows of different size you want in your post. You can use `auto` here too. Same as `grid-template-columns`, it helps you for row structure.

I used columns & some rows in my page. But honestly, they are looking like a matrix or table with no space & padding. Seems not so good to me. Okay don't give you up as you have `grid-gap` with you! Yess, it adds padding or space in your rows & columns. Now it's decent no?

> Remember container is to whom you have used `display:grid` property, then by all means it's nothing but `Grid Container` & children of container are `Grid-items`
