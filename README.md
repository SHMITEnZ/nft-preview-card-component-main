# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./screenshots/Screenshot%20NFT%20preview%20card%20component.png)

### Links

- Solution URL: [https://github.com/SHMITEnZ/nft-preview-card-component-main](https://github.com/SHMITEnZ/nft-preview-card-component-main)
- Live Site URL: [https://shmitenz.github.io/nft-preview-card-component-main/](https://shmitenz.github.io/nft-preview-card-component-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- BEM

### What I learned

Below the code I used to create the overlay effect

```html
<div class="card__container">
      <a href="#">
        <img class="card__container__image" src="./images/image-equilibrium.jpg" alt="equilibrium nft">
      </a>
      <img class="card__container__icon" src="./images/icon-view.svg" alt="eye-icon">
      <div class="card__container--overlay"></div>
    </div>
```
```css
.card__container{
    position: relative;
    width:100%;
}

.card__container--overlay{
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: .3s ease;
  background-color: var(--Cyan-);
}

.card__container__icon{
  position: absolute;
  text-align: center;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  opacity: 0;
}

/*active states*/

.card__container:hover .card__container__icon{
    opacity:1;
    z-index: 1;
}

.card__container:hover .card__container--overlay {
    opacity: 0.5;
} 

```

### Useful resources

- [w3 School](https://www.w3schools.com/howto/howto_css_image_overlay_icon.asp) - How TO - Image Overlay Icon

## Author

- Github - [SHMITEnZ](https://github.com/SHMITEnZ)
- Frontend Mentor - [@SHMITEnz](https://www.frontendmentor.io/profile/SHMITEnZ)
