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

### 1.2 Implicit Vs Explicit Grid

Now the basic fundamentals are clear, we can dive in further stuff. One of the important thing to know about grid is it's type i.e. Implicit & Explicit. Look below the simple grid creation of a container.

```css
.container {
  display: grid;
  grid-gap: 20px;
  grid-template-columns: 200px 400px;
  grid-template-rows: 50px 100px;
}
```

Yeah as you see, we have created two columns of size 200px & 400px using `grid-template-columns` and two rows of size 50px & 100px with help of `grid-template-rows` declaration.

Now that's where the game begins, you declare rows and columns with their size but yet there is another row with different row size. How?

When you declare a grid with specific columns and rows then that's `Explicit Grid` and when you don't, off course it's `Implicit Grid`. In this scenario, after two rows, the automatically generated rows have default size. You can clearly distinguish between implicit and explicit grid with help of Dev Tools. You can do so in firefox in the layouts section. Explicit grid starts & ends with `bold` line while implicit with faint `dash` line.

![Implicit Vs Explicit](./Images/grid.png)

Well in case if you don't want the default size for the implicit grid, then you can use the following properties to obtain desired results.

```css
.container {
  display: grid;
  grid-gap: 20px;
  grid-template-columns: 200px 400px;
  grid-template-rows: 50px 100px;
  grid-auto-rows: 80px;
  grid-auto-columns: 100px;
}
```

Property named `grid-auto-rows: 80px` adjusts the size of every implicit grid row. One thing to point out, we used `grid-auto-columns` but yet there is no extra specified column out there. Strange, isn't it?


### 1.3 Grid AutoFlow

Wondering why `grid-auto-columns` isn't working at all? Then you are at right place. Let's crack this down. Here we go.

When grid is implicit, then whatsoever elements that are out of explicit are automatically generated & placed as row rather a column. Know why? This is all because of `grid-auto-flow` which is by default set to `row`. And hence you didn't see any change in earlier example.

If you change 'grid-auto-flow' to 'column', then you can clearly catch those changes as all of your elements will be arranged column wise. Here is the snippet to get such result

```css
.container {
  display: grid;
  grid-gap: 20px;
  grid-template-columns: 100px;
  grid-template-rows: 100px;
  grid-auto-flow: column;
}
```
> The `grid-auto-flow` does the same functionality as the `flex-direction` in flexbox. It's completely one's choice to use any of them.  

Ever used instagram? I know it's not even a question worth asking. But why I mentioned gram here is notable. Seen Stroies? Yes, you have. Well you can create a gram story bar using a grid in a few steps without dealing with position and all. How? Pay a look down here.

```css
.container {
  display: grid;
  grid-gap: 20px;
  grid-template-columns: 100px;
  grid-template-rows: 100px;
  grid-auto-flow: column;
}

.item {
  border-radius: 50%;
}
```
Not to forget, you can use flexbox too. Remember, there are many ways to create the same thing. You got this. 
