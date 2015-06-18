## Website Performance Optimization portfolio project

#### Steps To View The Website

Some useful tips to help you get started:

1. Check out the repository
1. To inspect the site on your phone, you can run a local server

  ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```

1. Open a browser and visit localhost:8080
1. Download and install [ngrok](https://ngrok.com/) to make your local server accessible remotely.

  ``` bash
  $> cd /path/to/your-project-folder
  $> ngrok 8080
  ```

1. Copy the public URL ngrok gives you and try running it through PageSpeed Insights! Optional: [More on integrating ngrok, Grunt and PageSpeed.](http://www.jamescryer.com/2014/06/12/grunt-pagespeed-and-ngrok-locally-testing/)

Profile, optimize, measure... and then lather, rinse, and repeat. Good luck!

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

