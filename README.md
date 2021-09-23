# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Four card feature section solution](#frontend-mentor---four-card-feature-section-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Useful resources](#useful-resources)
  - [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

![](./screenshot.jpg)

## My process

### Built with

- SASS
- Flexbox
- CSS Grid

### What I learned

The first thing that came to mind when looking at the challenge was "How can I make the cards positioned like that in the desktop view?". I learned that I could use grid and flex at the same time to achieve that kind of layout.

I made 1x3 grid template with a mindset like this:
- Because the first and the third column only have 1 card each, I just needed to make sure that the cards were aligned center vertically (using flexbox).
- The second column has 2 cards in it and I wanted them to be on top of each other. Flexbox used as the solution to that.
  
```scss
.card-container {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;

    .first-col, .third-col {
        display: flex;
        align-items: center;
    }

    .second-col {
        display: flex;
        flex-direction: column;
    }
}
```

But after thinking for a little bit, I think you don't really need grid system when there is only one row. Flex might be enough here.

### Useful resources

- [Sass Guidelines](https://sass-guidelin.es/) - These guidelines helped me for managing my scss files and how to use mixins and variables.

## Author

- Frontend Mentor - [@calvindalenta](https://www.frontendmentor.io/profile/calvindalenta)
- LinkedIn - [@calvindalenta](https://www.linkedin.com/in/calvindalenta/)