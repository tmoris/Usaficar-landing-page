# Usaficar-landing-page
 Car washing and detailinng landing page

# The Odin Project foundations-landing page project

This is a solution to the [The Odin Project foundations-landing page project](https://www.https://www.theodinproject.com/lessons/foundations-landing-page). It is for helping me improve my coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)



## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- View services offered by the company
-Contact the site owners 

### Screenshot

![![image](https://user-images.githubusercontent.com/57036823/181718677-839b9bd4-33d9-4002-b474-7da252958549.png)
]

### Links

- Solution URL: https://github.com/tmoris/odin-recipes
- Live Site URL:https://tmoris.github.io/odin-recipes/

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
-scss 
- JS
- DOM


### What I learned

While working on this project i have learnt
how to; access elements in the DOM, use array function in JS, use CSS grid for styling page  and create reponsive layouts.
I have also learnt;  how organize work using scss partial files,  use of mixins and accessing of scss variables using @use


For code snippets examples, see below:

```scss
 $breakpoints: (
  'small': 20em,
  'medium': 48em,
  'large': 64em,
);

@mixin small-screen {
  @media (min-width: map-get($breakpoints, 'small')) {
    @content;
  }
}

@mixin medium-screen {
  @media (min-width: map-get($breakpoints, 'medium')) {
    @content;
  }
}

@mixin large-screen {
  @media (min-width: map-get($breakpoints, 'large')) {
    @content;
  }
}

application of mixin
.brand-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    
    &__nav {
      background-color: v.$black;
      color: v.$lightgrey;
      position: fixed;
      top: 0;
      right: 0;
      left: 10%;
      bottom: 0;
      transform: translateX(100%);
      transition: transform 250ms cubic-bezier(0.47, 0, 0.745, 0.715);

      @include m.medium-screen {
        transform: translateX(0);
        background-color: inherit;
        position: static;
        z-index: 1;
      }
    }
  

```
```js
const menuToggle = document.querySelector('.brand-nav__menu');
const links = document.querySelectorAll('.navlist__item--link');
menuToggle.addEventListener('click', () =>{
document.body.classList.toggle('open');
});
links.forEach(link => {
  link.addEventListener('click', () => {
document.body.classList.remove('open');
  });
});
```

### Useful resources

- [web.dev](https://web.dev/learn/css/) - This helped me learn mordern CSS techniques. I really liked the content and will use it going forward.
- [kevinpowell](https://courses.kevinpowell.co/conquering-responsive-layouts) - This is an amazing course which helped me finally understand responsive web design. I'd recommend it to anyone still learning this concept.



## Author

- Github - [@tmoris]https://github.com/tmoris
- Frontend Mentor - [@tmoris](https://www.frontendmentor.io/profile/tmoris)
- Twitter - [@tibenkanamoris](https://www.twitter.com/tibenkanamoris)


