# udacity-web-opt
Web Optimization project for Udacity's Front-End Nanodegree

#Project Description
The goal of this project was to optimize the performance of two files in <a href="https://github.com/cameronwp/udportfolio" target="_blank">this repo</a>.

To view the difference between the original and optimized files, check the links below:<br>

<a href="https://cdn.rawgit.com/cameronwp/udportfolio/master/index.html" target="_blank">original index.html file</a> | <a href="https://cdn.rawgit.com/anavasquez84/udacity-web-opt/master/index.html" target="_blank">optimized index.html file</a><br>
<a href="https://cdn.rawgit.com/cameronwp/udportfolio/master/views/pizza.html" target="_blank">original pizza.html file</a> | <a href="https://cdn.rawgit.com/anavasquez84/udacity-web-opt/master/views/pizza.html" target="_blank">optimized pizza.html file</a>

#Index.html
Changes on this file were done to improve the critical rendering path. Performance optimizations take this file's PageSpeed score from 30 to 95.  

<b>Optmizations</b><br>
1. Added media attribute to link <b>css/print.css</b><br>
2. Google Fonts were moved to <b>style.css</b> and are accessed using @font-face<br>
3.<b> Style.css</b> content was inlined and minified into <b>index.html</b><br>
4. Images from <b>line 16</b> and <b>line 46</b> were compressed and resized using ImageMagik<br>
5. JavaScript was minified and moved to the bottom of the page


#Pizza.html
Changes in this file were done to improve the FPS (frame-per-second) rate to 60FPS while scrolling. Changes were made to the file <b>views/js/main.js</b>

<b>Optimizations</b><br>
1. On <b>line 451</b> the <b>changePizzaSizes<b> function was refactored and updated 
2. On <b>line 526</b> the <b>updatePositions</b> function was refactored by debouncing scroll events<br>
3. On <b>line 556</b> <b>var items</b> was refactored to separate the loop from <b>items.length</b> and <b>scrollTop</b></br> 4. On <b>line 556</b>, <b>querySelectorAll</b> was changed to <b>getElementsByClassName</b> <br> 5. On <b>line 579</b>, <b>requestAnimationFrame</b> was added to optimize rendering <br> 6. On <b>line 587</b>, pizza quantity was reduced to 40.  

#Resources
The following pages were used as resources

https://css-tricks.com/snippets/css/using-font-face/<br>
http://www.jsmini.com/?_ga=1.63345127.99162416.1424805980<br>
http://www.cleancss.com/css-minify/?_ga=1.132248461.2019049402.1435843830<br>
http://www.html5rocks.com/en/tutorials/speed/animations/<br>
http://stackoverflow.com/questions/29979787/javascript-how-can-i-optimize-this-line-for
