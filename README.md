## Website Performance Optimization portfolio project

#### Steps To View The Website

This site is on git hub pages. 

1. Visit the url:

http://rdgrmcore.github.io/frontend-nanodegree-mobile-portfolio/

Be sure to run index.html

### Optimizations Performed

#### Scrolling
The function updatePositions was causing a synchronous layout. I moved the 
read of the document.body.scrollTop out of the for loop. 

Pre calculate values for phases.

Use getElementsByClassName as a selector.

Use transform translateX instead of basicLeft.

Only draw as many background pizzas as needed.


#### Resize Pizzas
Create a randomPizzas variable to avoid repeating the querySelectorAll.

Don't call determineDx.

Use a switch statement to set the width % without converting between pixels and %.

