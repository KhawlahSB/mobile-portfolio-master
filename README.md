## Website Performance Optimization portfolio project

Project to optimize website based on frame rate and google pagespeed insights scores

###Optimize PageSpeed Insights

- Minify CSS and JS files
- Optimize size and compression of images
- Eliminate render-blocking JavaScript and CSS in index.html
- style.css is inlined in index.html. and print.css now have media=print tag.
- Put the Google Analytics script to the footer of the page.


###Optimize Frame Rate
- changes in views/js/main.js:
- Put 'use strict'  mode for the whole script syntax to make the code more secure.
- Selectors querySelector and querySelectorAll replaced with getElementById and getElementsByClassName,it's faster.
- Optimize the loops
- Create all the variables outside of loops where possible.
- Declaring the variable in the initialisation of the for-loops as prevention from being created every time the loop is executed.
- Dynamically calculate the number of pizzas needed to fill the screen, based on browser window resolution


###How to use and test the app and performance

#### 1. Optimize PageSpeed Insights score for index.html

Download the repository

Run it on a local server:

$> cd /path/to/your-project-folder
$> python GzipSimpleHttpServer.py
Open a browser and visit localhost:8000

$> cd /path/to/your-project-folder
$> ./ngrok http 8000
Copy the public URL ngrok gives you and try running it through PageSpeed Insights!

#### 2. Optimize Frames per Second in pizza.html

Open views/pizza.html in a chrome browser

In developer tools navigate to timeline

Record a timeline and check the FPS values on the graph

-----------------------------------------------
index.html achieves a PageSpeed score of at least 90 for Mobile and Desktop
Pizza.html should be rendered with a consistent frame-rate at 60fps when scrolling.
Time to resize pizzas is less than 5 ms

