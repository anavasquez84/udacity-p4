# Web Optimization
Project 4 for Udacity's Front-End Nanodegree

#####Project Description
The goal of this project was to optimize the performance of two files in [this repo](https://github.com/cameronwp/udportfolio)

To view the difference between the original and optimized files, check the links below:

[original index.html file](https://cdn.rawgit.com/cameronwp/udportfolio/master/index.html) | [optimized index.html file](https://cdn.rawgit.com/anavasquez84/udacity-web-opt/master/index.html)

[original pizza.html](https://cdn.rawgit.com/cameronwp/udportfolio/master/views/pizza.html) | [optimized pizza.html file](https://cdn.rawgit.com/anavasquez84/udacity-web-opt/master/views/pizza.html)

#####Index.html
Changes on this file were done to improve the critical rendering path. Performance optimizations take this file's PageSpeed score from 30 to 93.  

**Optmizations**

1. Added media attribute to link **css/print.css**
2. Google Fonts were moved to **style.css** and are accessed using @font-face
3. **Style.css** content was inlined and minified into **index.html**
4. Images from **line 16** and **line 46** were compressed and resized using ImageMagik
5. JavaScript was minified and moved to the bottom of the page

#####Pizza.html
Changes in this file were done to improve the FPS (frame-per-second) rate to 60FPS while scrolling. Changes were made to the file **views/js/main.js**

**Optimizations**

1. On **line 451** the **changePizzaSizes** function was refactored and updated 
2. On **line 526** the *updatePositions* function was refactored by debouncing scroll events
3. On **line 556** **var items** was refactored to separate the loop from **items.length** and **scrollTop**
4. On **line 556**, **querySelectorAll** was changed to **getElementsByClassName** 
5. On **line 579**, **requestAnimationFrame** was added to optimize rendering 
6. On **line 587**, pizza quantity was reduced to 40.  

#####Resources
The following pages were used as resources:

[https://css-tricks.com/snippets/css/using-font-face/](https://css-tricks.com/snippets/css/using-font-face/)
[http://www.jsmini.com/?_ga=1.63345127.99162416.1424805980](http://www.jsmini.com/?_ga=1.63345127.99162416.1424805980)
[http://www.cleancss.com/css-minify/?_ga=1.132248461.2019049402.1435843830](http://www.cleancss.com/css-minify/?_ga=1.132248461.2019049402.1435843830)
[http://www.html5rocks.com/en/tutorials/speed/animations/](http://www.html5rocks.com/en/tutorials/speed/animations/)
[http://stackoverflow.com/questions/29979787/javascript-how-can-i-optimize-this-line-for](http://stackoverflow.com/questions/29979787/javascript-how-can-i-optimize-this-line-for)
