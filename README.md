# Frontend Mentor - Bento grid solution

This is a solution to the [Bento grid challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Bento grid solution](#frontend-mentor---bento-grid-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
  - [Author](#author)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size

### Links

- Solution URL: [Github Repository](https://github.com/twx0504/Bento-Grid-Component)
- Live Site URL: [Live](https://twx0504.github.io/Bento-Grid-Component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Grid
- Desktop-first workflow

### What I learned
1. I followed the Desktop-First Responsive Design philosophy with CSS Grid. I learnt to change the layout on different breakpoints.
```css 
/* Layout */
.bento-grid-container {
  display: grid;
  grid-template-columns:
    minmax(25.6rem, 1fr) minmax(25.6rem, 1fr) minmax(25.6rem, 1fr)
    minmax(25.6rem, 1fr);
  grid-template-rows: repeat(3, 28.4rem);
  grid-template-areas:
    "column-1 column-2 column-2 column-3"
    "column-1 column-2 column-2 column-3"
    "column-1 column-4 column-5 column-5";
  gap: var(--spacing-400);
  padding: var(--spacing-400);
}

@media screen and (max-width: 1200px) { 
  /* Layout */
  .bento-grid-container {
    min-width: 68.8rem;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: auto;
    grid-template-areas:
      "column-2 column-2"
      "column-3 column-3"
      "column-5 column-5"
      "column-4 column-4"
      "column-1 column-1";
  }
}

@media screen and (max-width: 576px) { 
  .bento-grid-container {
    /* Reset min-width*/
    min-width: fit-content;
    /* Clear the definition of grid-template-areas */
    grid-template-areas: none;
    grid-template-columns: 1fr;
  }
}
```
2. I learnt that to set the size of html and body element when the html and body element size do not fit the content.
```css
html {
  /* Set the default height */
  height: 100%;
}

body {
  /* Body */
  /* let body uses the available space */
  min-width: fit-content;
  /* Ensure the max width stretch to the entire viewport width */
  max-width: 100vw;
  /* Inherit height from html.  */
  min-height: 100%;
}
```

## Author

- GitHub - [Too Wei Xin](https://github.com/twx0504)
- Frontend Mentor - [@twx0504](https://www.frontendmentor.io/profile/twx0504)