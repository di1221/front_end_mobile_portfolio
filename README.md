## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).


******** Accepted the challenge! *************


#####  Steps to run application ##########
1. user navigates to the index page
2. user can click on any of the 4 links on the index page to see more content on other HTML pages.
3. user clicks on Cams Pizzeria (must use this link for testing both sections of the project) and
  will then land on the pizza.html page.
4. Several buttons at top of the page take the user to those sections of the page (except contact us)
5. When user scrolls down the page the pizza images (foreground and background) move locations on the page.
6.  There is a slider bar that has 3 positions for pizza size large/medium/small.  Moving the slider
  changes the size label to one of those 3 sizes, and correspondingly changes the size of the foreground pizza images.


#### Optimizations on main.js ############
-- using getElementById instead of querySelector for label change on pizza resize
-- Changes the slider value to a percent width
-- change pizza size function changes:
     removed unnecessary calculations
     pulled length calculations out of the repetitive loop causing forced asynchronous layouts
-- in update pizza position function :
     reduced the # of times from 200 to 25 for updating positions
     removed unnecessary for loop


##### Changed the following #####
1. added character set to header in pizza.html.  It was already present in the other html files
2. moved js script tag  before the links to external scripts.
3. moved all js script tags to the end of the index.html file
4. optimized images and Saved down to 488.5KB out of 3MB. 27% per file on average (up to 67.7%)
5. optimized order of styles and scripts
6. specified image dimensions


#### Tools used ##########
1. Image Optum - to optimize images
2. Photoshop - for some of the image optimization/compression
3. Used my Samsung phone for additional (also used device mode in dev tools) Android testing
4. Timeline - in dev tools
5. http://cssminifier.com/
6. Grunt -
    using plug-in's:
       contrib-jshint (to validate javascript),
       contrib-uglify (to minify javascript),
       contrib-concat (to concatenate src files),
       contrib-watch (to watch for any changes I was making to js files)
7. ngrok


##### Resources Used ############
http://cssminifier.com/
https://www.udacity.com -
      Website Performance Optimization & Browser Rendering Optimization courses,
https://developers.google.com (especially PageSpeed insights and analyzing crp perf sections),
http://gruntjs.com,
https://www.npmjs.com/



####### Page Speed Results ########
changed overall PageSpeed results from 99 (97 on mobile device / user experience 100 on mobile)





******* pizza resize and scrolling #################
changed the interation for the changePizzaSizes function - to prevent multiple forced
----  synchronous layouts
optimized pizza and pizzeria jpg's

reduced time to resize pizzas: < .7ms (on average)
fps is consistently below 40 fps







# -frontend-nanodegree-mobile-portfolio
