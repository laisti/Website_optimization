## Website Performance Optimization portfolio project

My challenge was to optimize the online portfolio https://github.com/udacity/frontend-nanodegree-mobile-portfolio for speed.

### Getting started

There are two directories: development and production.
"development" directory consists of files for development goals, "production" - for website optimization.

1. Download this repository to your local computer
2. Install and configure any webserver on your computer, for example python, or apache, or another one.
3. Copy contents of "production" directory to the root directory of your webserver.
4. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok http 80
  ```
5. Open a browser and visit localhost:80

### What have done

In this project, I have made some optimizations.

In index.html and views/pizza.html:

- Identified and performed optimizations to achieve a PageSpeed score over 90
- Ensured a consistent framerate of 60 FPS for views/pizza.html
- Reduced time to resize pizzas in views/pizza.html to < 5ms
- Resized and compressed images to reduce bandwidth
- Inlined above-the-fold CSS and made JavaScript load asynchronously to eliminate render-blocking
- Minified of static resources

In views/css/style.css:

- Added "@media all" to prioritize what content will be rendered first on mobile devices
- Set .mover to "will-change: transform;" to reduce repainting time by set images on their own levels

In views/js/main.js:

- Changed maximum amount of pizzas in addEventListener
- Changed all uses of querySelectorAll to getElementsByClassName
- Pulled calculation of constants out of loop in function updatePositions()
- Moved variables: "items" and "pizzasDiv", out of the function updatePositions() and out of loop, accordingly
- Changed function changePizzaSizes(size) to reduce time of resizing pizzas in views/pizza.html to < 5ms


