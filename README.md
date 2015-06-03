## Website Performance Optimization portfolio project

Note: The original README.md is [here](https://github.com/dougconner/frontend-nanodegree-mobile-portfolio).

The application is running on [Github](http://dougconner.github.io/frontend-nanodegree-mobile-portfolio/).

### Optimizations performed on views/js/main.js

1. Converted pizza size slider to percent width. Refactored changePizzaSize() by more efficiently computing the newwidth value, using a more efficient selector (.getElementByClassName), and brought the selector outside the for-loop.

2. Brought the document.getElementById(“randomPizzas”) outside the for-loop for creating the random pizzas to improve page load. No effect on FPS speed.

3. Modified updatePositions() to generate more of the phase computation outside the for-loop.

4. Modified the code that runs when the page loads or resizes to only add background pizzas in the visible window (typically 16 - 24 depending on window height) instead of 200. Also moved the selector outside the for-loop and changed the selector to the more efficient (.getElementById instead of .querySelector). These changes include the generatePizzas() function, and adding an eventListener for window resize.

5. A style sheet change was also made to use separate layers for the backgroud pizzas to improve the FPS response.

### Build tools

I used the [CodeKit](https://incident57.com/codekit/index.html) build tool on this project after evaluating several build tools. Currently I am using the tool's minifier to minify the views/js/main.js file. The minified file is automatically generated after each save on Sublime. I also have the tool checking syntax with JSHint and reloading after every source code save. I have changed pizza.html before submission to use the minified JS. The build tool has a lot of capability that I am still learning to use.