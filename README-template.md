# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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


## Overview
### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size



### Links

- Live Site URL: https://jolly-yeot-8ce6bd.netlify.app/

## My process
I decided to divide in three different sizes. I apply mobile-first technique and used media queries to adapt the others two sizes Ipad and desktop screen.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned
I had a great challenge centering the main div cause I was using flexbox to established the footer at the end of the page.
body{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;

.attribution{
    margin-top: 50px;
}

And when I typed 
wrapper{
width:80%;
 the flow got broken and both of the children  "wrapper" and "attribution" were not working as it supposed to be vertically but horizontally like a row. I reallized that the problem was that I was not using 100% and that was the reason cause the flow was not fucntioning correctly so I decided to keep the 100% in wrapper but type 80% in container the only-child of wrapper.


 .container{
    width: 85%;
    margin: auto;
}

On the other hand, other challenged that it kept me wracking my head for a while was that my content did not adjust correctly to the grid columns. I had this.
.container {
        display: grid;
        gap: 10px;
        grid-template-areas:
            "Daniel Daniel Jonathan Kira"
            "Jeanette Patrick Patrick Kira";
    }

Obviusly I specified the name of the grid area before defining the area template but it didn´t work. After a long period of time trying to puzzle it . I realized that the content of the columns inside the template-areas does not work correctly if I don´t define grid template columns and grid template rows. But mainly was because cthe columns for some reason it worked when I gave sizes to each column defined inside the grid-template-area.

.container {
        padding: 0 30px;
        display: grid;
        grid-template-columns: repeat(4, minmax(100px, 1fr)); The problem was that I was not giving 4 sizes but 3 cause it slipped of my head the real number
        grid-template-rows: 1fr 1fr;
        gap: 10px;
        grid-template-areas:
            "Daniel Daniel Jonathan Kira"
            "Jeanette Patrick Patrick Kira";
    }

