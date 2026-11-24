# Frontend Mentor - Blog preview card solution

This is my solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS).

## Table of contents

- [Overview](#overview)
- [My process](#my-process)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Links

- Solution URL: [GitHub repository](https://github.com/sojib-hasan04/blog-preview-card)
- Live Site URL: [Netlify](https://brilliant-florentine-c71343.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- BEM-style class names
- Google Fonts (Figtree)

### What I learned

**1. Choosing HTML tags by purpose, not by looks.**
The "Learning" label looks like a button, but it is not clickable, so I used a `<span>` instead of a `<button>`. I also used `<article>` for the card, `<time datetime="2023-12-21">` for the date, and put an `<a>` inside the `<h1>` because the title is the interactive element in the design.

**2. HTML `width`/`height` vs CSS `width`.**
I added each image's natural size (found with `naturalWidth` and `naturalHeight` in the browser console) to the `<img>` tags to prevent layout shift. The size on screen is controlled by CSS (`width: 100%`), and CSS wins over the HTML attributes.

**3. Why `box-sizing: border-box` matters.**
Without it, the card's padding was added on top of `max-width`, so the card became wider than I wanted.

**4. `inline` vs `inline-block`.**
The tag needed its own size plus vertical padding and margin, so `display: inline-block` worked better than `inline`.

**5. A missing `}` breaks everything below it.**
I forgot to close the `.card` rule, so the browser treated all the following rules as nested. My footer lost its styles. Checking the braces fixed it.

**6. Links have default styles.**
Wrapping the title in `<a>` made it blue and underlined. I fixed it with `.card__heading a { text-decoration: none; color: inherit; }` and added `:hover` and `:focus-visible` styles so keyboard users can see where they are.

**7. Other habits I practiced.**
Using `rem` instead of `px`, naming classes by what the element does (`card__title`, `card__author`), keeping all CSS in `style.css`, and using empty `alt=""` for decorative images.

**8. Git basics.**
`git init`, `git add` with file names (to avoid adding the `.idea` folder), `git commit`, connecting a remote, and `git push`. Then deploying from GitHub to Netlify.

### Continued development

- Self-hosting the Figtree font with `@font-face` instead of the Google Fonts link
- Learning `clamp()` for responsive font sizes
- Testing the layout at more screen sizes, including the desktop design

### AI Collaboration

I used Claude as a mentor while building this project. It gave me hints, explained why things behave the way they do, and helped me find mistakes (like the missing `}`). I wrote most of the HTML structure and CSS myself, but I also got some short code snippets from Claude, such as the hover/focus rule, the `<time>` tag, and the font link. I checked each one in the browser to see what it does.

## Author

- GitHub - [@sojib-hasan04](https://github.com/sojib-hasan04)
- Frontend Mentor - [@sojib-hasan04](https://www.frontendmentor.io/profile/sojib-hasan04)