## Website Performance Optimization portfolio project


### Getting started:
To run the application, unzip the zip package and double click the index.html file.  The page will open in your browser.

### Optimisations made to index.html:
* images optimised using [PageSpeed Insights](https://developers.google.com/speed/pagespeed/insights/)
* asynchronous load of JavaScript where applicable
* used [web font loader](https://github.com/typekit/webfontloader) for web fonts
* inlined the CSS where applicable
* used media=print for print.css


### Optimisations made to main.js:

####Pizza Size slider
* created variable 'pizzaSizeSelector' for document.getElementsByClassName("randomPizzaContainer"); and removed this from the loop. [credit](https://www.w3schools.com/js/js_performance.asp)
* changed document.querySelectorAll to getElementsByClassName.  [credit](https://www.reddit.com/r/learnjavascript/comments/356k1v/confused_on_queryselector_and_getelementbyid/)
* changed sizeSwitcher function to remove previous dx function.  now modified style to % width.  credit: cam's classroom example & [credit](https://www.w3schools.com/js/js_switch.asp)

#### updatePositions
* created variable 'l' for items.length and took this outside of the loop.  [credit](https://www.w3schools.com/js/js_performance.asp)
* created variable 'scroll' for document.body.scrollTop and took this outside of the loop.  [credit](https://www.w3schools.com/js/js_performance.asp)
* changed .querySelectorAll to getElementsByClassName.  [credit](https://www.reddit.com/r/learnjavascript/comments/356k1v/confused_on_queryselector_and_getelementbyid/)
* changed style.left to style.transform [credit](https://discussions.udacity.com/t/replace-left-with-transform/20093)
* used requestAnimationFrame to updatePositions on scroll.  [credit](http://www.html5rocks.com/en/tutorials/speed/animations/)

#### Generate pizzas on load
* created variable 'movingPizza' for document.getElementById and took this outside of the loop. [credit](https://www.w3schools.com/js/js_performance.asp)
* Changed .querySelector to getElementById
* changed i<200 to i<45 to reduce the number of background pizzas
