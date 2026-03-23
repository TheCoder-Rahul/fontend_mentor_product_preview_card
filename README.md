# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![Design screenshot](https://github.com/TheCoder-Rahul/fontend_mentor_product_preview_card/blob/main/project_screenshot.png)

### Links

- 👉 [Solution URL](https://github.com/TheCoder-Rahul/fontend_mentor_product_preview_card.git)
- 👉 [Live Site URL](https://thecoder-rahul.github.io/fontend_mentor_product_preview_card/)

## My process

### Built with

- 👉 **Markup:** Semantic HTML5 for better accessibility and SEO.
- 👉 **Styling:** CSS3 with Custom Properties (variables) for a maintainable color scheme, font-properties, and different sizes.
- 👉 **Layout:** Flexbox for centering the card and managing the internal alignment.
- 👉 **Workflow:** Mobile-first approach and Responsive Design using Media Queries.

### What I learned

Check the code snippets attached below:

```html
<main>
  <article>
    <section class="product-image">
      <img class="mob_dev_img" src="./images/image-product-mobile.jpg" alt="Gabrielle Chanel Perfume Bottle" loading="lazy" />
      <img class="dsk_dev_img" src="./images/image-product-desktop.jpg" alt="Gabrielle Chanel Perfume Bottle" loading="lazy" />
    </section>
    <section class="product-info">
      <h2>Perfume</h2>
      <h1>Gabrielle Essence Eau De Parfum</h1>
      <p>A floral, solar and voluptuous interpretation composed by Olivier Polge, Perfumer-Creator for the House of CHANEL.</p>
      <p class="price">
        <span class="current-price">$149.99</span>
        <span class="original-price">$169.99</span>
      </p>
      <button type="button" class="add-to-cart"><svg width="15" height="16" xmlns="http://www.w3.org/2000/svg"><path fill="#FFF" d="M14.383 10.388a2.397 2.397 0 0 0-1.518-2.222l1.494-5.593a.8.8 0 0 0-.144-.695.8.8 0 0 0-.631-.28H2.637L2.373.591A.8.8 0 0 0 1.598 0H0v1.598h.983l1.982 7.4a.8.8 0 0 0 .799.59h8.222a.8.8 0 0 1 0 1.599H1.598a.8.8 0 1 0 0 1.598h.943a2.397 2.397 0 1 0 4.507 0h1.885a2.397 2.397 0 1 0 4.331-.376 2.397 2.397 0 0 0 1.12-2.021ZM11.26 7.99H4.395L3.068 3.196h9.477L11.26 7.991Zm-6.465 6.392a.8.8 0 1 1 0-1.598.8.8 0 0 1 0 1.598Zm6.393 0a.8.8 0 1 1 0-1.598.8.8 0 0 1 0 1.598Z"/></svg>Add to Cart</button>
    </section>
  </article>
</main>
```
```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
:root {
  --bold-font: 700;
  --medium-font: 500;
  --fs-big: 1.75rem;
  --fs-small: 0.75rem;
  --fs-primary: 0.875rem;
  --clr-white: hsl(0, 0%, 100%);
  --clr-body-bg: hsl(30, 38%, 92%);
  --clr-primary: hsl(158, 36%, 37%);
  --clr-neutral: hsl(212, 21%, 14%);
  --clr-secondary: hsl(228, 12%, 48%);
  --clr-primary-dark: hsl(158, 42%, 18%);
  --secondary-font: 'Fraunces', serif;
  --primary-font: 'Montserrat', sans-serif;
}
body {
  display: flex;
  height: 100vh;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  color: var(--clr-secondary);
  font-family: var(--primary-font);
  background-color: var(--clr-body-bg);
}
article {
  display: flex;
  margin: 0 auto;
  overflow: hidden;
  border-radius: 0.5rem;
  width: min(610px, 94%);
  flex-direction: column;
  background-color: var(--clr-white);
}
article img {
  width: 100%;
  height: auto;
  display: flex;
}
article img.dsk_dev_img {
  display: none;
}
.product-info {
  gap: 1rem;
  display: flex;
  padding: 1.5rem;
  flex-direction: column;
}
.product-info h1 {
  line-height: 1;
  font-size: var(--fs-big);
  color: var(--clr-neutral);
  font-weight: var(--bold-font);
  font-family: var(--secondary-font);
}
.product-info h2 {
  font-weight: 400;
  letter-spacing: 3px;
  text-transform: uppercase;
  font-size: var(--fs-small);
}
.product-info p {
  line-height: 1.5;
  font-size: var(--fs-primary);
  font-weight: var(--medium-font);
}
.product-info p.price {
  gap: 1rem;
  display: flex;
  align-items: center;
}
.product-info p.price .current-price {
  font-size: var(--fs-big);
  color: var(--clr-primary);
  font-weight: var(--bold-font);
  font-family: var(--secondary-font);
}
.product-info p.price .original-price {
  font-size: var(--fs-small);
  color: var(--clr-secondary);
  text-decoration: line-through;
}
.add-to-cart {
  gap: 0.5rem;
  width: 100%;
  border: none;
  display: flex;
  padding: 1rem;
  cursor: pointer;
  font-weight: 600;
  align-items: center;
  font-size: 0.875rem;
  border-radius: 0.5rem;
  justify-content: center;
  color: var(--clr-white);
  font-family: var(--primary-font);
  background-color: var(--clr-primary);
  -webkit-transition: all 0.3s ease-in-out;
  -moz-transition: all 0.3s ease-in-out;
  -ms-transition: all 0.3s ease-in-out;
  -o-transition: all 0.3s ease-in-out;
  transition: all 0.3s ease-in-out;
}
.add-to-cart:hover, .add-to-cart:focus, .add-to-cart:active {
  background-color: var(--clr-primary-dark);
}
.attribution { font-size: 11px; text-align: center; position: absolute; bottom: 1rem; }
.attribution a { color: var(--clr-primary); }

@media (min-width: 768px) {
  :root {
    --fs-big: 2.25rem;
    --fs-primary: 1rem;
    --fs-small: 0.875rem;
  }
  article {
    flex-direction: row;
  }
  article > section {
    flex-basis: 50%;
  }
  article img.dsk_dev_img {
    display: block;
  }
  article img.mob_dev_img {
    display: none;
  }
  .product-info {
    gap: 1.5rem;
  }
  .product-info p.price {
    line-height: 1;
  }
}
```

## Author

- 👉 GitHub - [TheCoder-Rahul](https://github.com/TheCoder-Rahul)
- 👉 Frontend Mentor - [@TheCoder-Rahul](https://www.frontendmentor.io/profile/TheCoder-Rahul)
- 👉 LinkedIn - [@Rahul Kumar](https://www.linkedin.com/in/rahul-the-developer/)