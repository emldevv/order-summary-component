# Frontend Mentor - Order summary card solution

This is a solution to the [Order summary card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlPmajDUj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- See hover states for interactive elements

### Screenshot

![](./screenshot.jpg)

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process
I followed this general outline:
1. Boilerplates for html and CSS.
2. Structure html elements and items, adding classes and id's as much as I can before styling. Later I can edit classess and tags as they make more sense.
3. Start styling by building my custom properties menu. Then colours, fonts and styles in each section individually. I do this to preserve responsiveness as much as possible until I'm ready to position elements.
4. Positioning and sizing. When it comes to margins and padding, I tend to work top to bottom, rather than assigning each element more than one sizing property. For example, instead of all elements having a margin of 1em, the bottom of element a will have a margin bottom of 2em, element b and margin of 2 em, element c... so on and so forth. It makes it a lot easier to trouble shoot and edit.
5. Re-read style-guide and README for details on UI, and then add features.
6. Final touches.
### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

The bigger lessons in this project were

BACKGROUND IMAGE
  replacing:
  ```css
  background-img {
    ...
  }

  with: 
  body {
      background-image: url(images/pattern-background-mobile.svg);
      background-size: 100%;
  }
  ```
  This solved a problem I was having with the background image not falling behind the card. Adding 'background-size: 100%' solved the image repeating.

ADJUSTING THE BACKGROUND IMAGE
The image was the 'mobile-first' version, and therefore repeated on the desktop. Whilst a desktop version of the image was provided, I was playing around with what happens if I switch to desktop mode with a smaller image.
a. Doesn't fill space laterally
b. I want it only half the height of the page
b. Repeats
This is how I fe=ixed each:
  ```css
  body {
    /* min-width: 375px; */
    background-image: url(images/pattern-background-mobile.svg);
    background-size: 100% 50%;      /* a and b solved */
    background-repeat: no-repeat;   /* c solved*/
  }
  ```

FITING AND IMAGE INSIDE A CONTAINER'S DIMENSIONS  
  The image at the top of the card had been giving me a lot of headaches. It was too wide, causing scrolling, and would not fit the shape of the card container. I solved this with two css properties:

  1. Image fit to container width
  ```css
  .hero img {
   max-width: 100%;
  }
  ```
  2. Image clipped to container shape/dimensions
  ```css
  .order-summary-card {
    overflow: hidden;
  }
  ```

To see how you can add code snippets, see below:

```html
<h1>Some HTML code I'm proud of</h1>
```
```css
.proud-of-this-css {
  color: papayawhip;
}
```
```js
const proudOfThisFunc = () => {
  console.log('🎉')
}
```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
