<h1 align="center">Simple Feature Section</h1>

<div align="center">
   Solution for a challenge <a href="https://devchallenges.io/challenge/simple-feature-section-challenge" target="_blank">Simple Feature Section</a> from <a href="http://devchallenges.io" target="_blank">devChallenges.io</a>.
</div>

<div align="center">
  <h3>
    <a href="https://henrydevlab.github.io/simple-feature-section/">
      Demo
    </a>
    <span> | </span>
    <a href="https://github.com/Henrydevlab/simple-feature-section">
      Solution
    </a>
    <span> | </span>
    <a href="https://devchallenges.io/challenge/simple-feature-section-challenge">
      Challenge
    </a>
  </h3>
</div>

<!-- TABLE OF CONTENTS -->

## Table of Contents

- [Overview](#overview)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Built with](#built-with)
- [Features](#features)
- [Contact](#contact)

<!-- OVERVIEW -->

## Overview

![screenshot](screenshoot.png)

This project is a pixel-perfect, highly responsive feature grid interface designed to display SaaS product feedback mechanisms. It handles custom layout constraints, multi-density display ratios, and intentional typographic layouts smoothly across desktop, tablet, and mobile displays.

### What I learned

While building this challenge, I reinforced my knowledge of CSS line-clamping and multi-density responsive image engineering. 

To ensure that the vertical rhythm of the grid remained perfectly synchronized regardless of variations in text lengths, I utilized Webkit line-clamping rules coupled with a strict element height configuration:

```css
/* Forcing a consistent 3-line layout constraint for card descriptions */
.card__description {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
  height: 4.8rem;
  flex-grow: 1; /* Pushes the image container flush to the bottom edge */
}
```

Additionally, I learned how to deploy image-set() arrays inside CSS to provide multi-tier background asset routing. This allows the browser to selectively load @2x or @3x assets only when high-density viewports require it:

```css
body {
  background-image: image-set(
    url('resources/Background_image.svg') 1x,
    url('resources/Background_image@2x.png') 2x,
    url('resources/Background_image@3x.png') 3x
  );
}
```

### Useful resources

- [MDN Web Docs - Using image-set(](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Values/image/image-set) - This specification guide was essential in understanding how to serve optimized topographical background graphics across varying screen densities.
- [CSS-Tricks - Line Clamping](https://css-tricks.com/line-clampin/) - A comprehensive breakdown that helped me master text truncation techniques to match design-specific line wrapped requirements perfectly.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox (Layout Positioning)
- CSS Grid
- BEM (Block-Element-Modifier) Architecture Strategy

## Features

- **Pixel-Perfect Line Wrapping**: Leverages conditional layout utility classes to control text breaking across specified word junctions.
- **Dynamic Image Scaling**: Integrates srcset specifications on inner markup layouts to deliver 1x and 2x resolution options seamlessly.
- **Fluid Grid Collapsing**: Implements structural media queries at target viewport break marks to collapse horizontal rows into organized mobile list blocks.

## Contact

- GitHub [@henrydevlab](https://{github.com/henrydevlab})
