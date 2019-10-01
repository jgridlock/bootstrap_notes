# bootstrap_notes

# Bootstrap 4
## Overview
* Setup html doc with the following: https://getbootstrap.com/docs/4.0/getting-started/introduction/
* Basic structure of bootstrap is container, row, column.
	* IE webpage is the container, toolbar is the row and pages in the toolbar are the columns.
* Information about how the grid layout works: https://getbootstrap.com/docs/4.1/layout/grid/
## Containers
* Everything is applied via classes.
* Regular container has a width relative to a user's screen size, becomes horizontally centered and has a left and right margin.
```
<div class="container"></div>
```
* If we wanted the container to take up the entire width of the screen we can assign a class of container fluid.
```
<div class="container-fluid"></div>
```
* Note: Bootstrap uses CSS notation for classes, which entails having a ```.``` before a class name like ```.example-class-name```.
## Rows
* Rows are nested within containers. By default they take up the entire width:
```
<div class="container">
  <div class="row">
  </div>
</div>
```
## Columns
* Columns default to 12 and are broken down by 6, 4, 3, 2, 1. Better representation can be seen:
https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-4/simple-12-grid.svg
* Example code:
```
<div class="container">
  <div class="row">
    <div class="col">
    </div>
  </div>
</div> 
```
* Column customization can be done using col-#.
* If you want the content inside of the column to determine the width use col-auto. IE:
```
<div class="col-auto">
  <p>This content determines the width of the parent column</p>
</div>
```
* Boostrap breakpoints change the layout of content based on screen sizes. This can be incorporated using the following naming convention:
```
col-breakpoint-width
```
* An example would be:
```
col-sm-8
```
* The options are sm, md, lg, or xl. There is no xs because xs is the default size.
* We can mix and match multiple breakpoints:
```
<div class="col-12 col-md-8 col-xl-6"></div>
```
* From the example, we have a column that renders a different width based on a user’s screen size. On extra small and small sized screens, the column has a width of 12 individual columns. For medium and large sized screens, the column has a width of 8 individual columns. Lastly, for extra large screens, the column has a width of 6 individual columns.
## Colors
* Changing text color, more examples: https://getbootstrap.com/docs/4.2/utilities/colors/#color
```
<p class="text-primary">This text is blue!</p>
```
* Same logic applies for backgrounds: https://getbootstrap.com/docs/4.2/utilities/colors/#background-color
```
<div class="bg-success">
  Green! This signifies success! 
</div>
```
* To add text styling and wrapping: https://getbootstrap.com/docs/4.2/utilities/text/
```
<p class="font-weight-bold">
  This rendered text is bold.
</p>
```
```
<p class="font-weight-bold text-uppercase">
  This rendered text is both bold and uppercased. 
</p>
```
* To add positioning: https://getbootstrap.com/docs/4.2/utilities/position/
```
<div class="fixed-top">
  This div will be fixed at the top of the screen. 
</div>
```
## Components
* Setting class nav is for a toolbar. Use nav-link for each link.
* Buttons can be found in: https://getbootstrap.com/docs/4.2/components/buttons/#examples
```
<button type="button" class="btn btn-danger">Danger</button>
```
* Additional collapsing information: https://getbootstrap.com/docs/4.2/components/collapse/
```
<button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
  This button controls the following div's visibility. 
</button>

<div class="collapse" id="collapseExample">
  <p>This content's visibility gets toggled</p>
</div>
```
* In the example above, we have a <button> element that toggles the visibility of the <div> element below it.
The button has an attribute data-toggle="collapse" which enables button’s toggle ability. Another attribute, data-target="#collapseExample", means that this button toggles the visibility of the element with the id of "collapseExample". The aria-expanded and aria-controls attributes are information for screen readers and other accessibility means. Focusing our attention on the <div> below the button, notice that it has a class of "collapse", which hides the content when the webpage initially renders. Our <div> also has an id of "collapseExample" which corresponds to the value of the button’s data-target.
* NOTE: You can add a class called active to components so that they are not greyed out(disabled).
* Example navbar:
```
  <nav class="navbar navbar-expand-sm navbar-light bg-light">
    <!-- Add the <a> below: -->
    <a class="navbar-brand"><img src="https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-components/logo.png" alt="Gloria's Gardening Logo" height="30"></a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <!-- Make the follow elements into a nav component: -->
      <ul class="navbar-nav">
        <li class="nav-item active">
          <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Weekly Specials</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">About</a>
        </li>
      </ul>
    </div>
  </nav>
  ```
  * Bootstrap has a Jumbotron component for big displays:
```
    <div class="row">
      <div class="col">
        <!-- Add a jumbotron component below -->
        <div class="jumbotron">Roses</div>
      </div>
    </div>
  ```
  * Card components serves as a container for smaller customized content. Card components are often grouped together to display a collection of similar content in manageable chunks. We can draw a comparison of the card component to playing cards in deck — in both cases, there are cards grouped together and each one contains something different:
```
<div class="card">
  <img class="card-img-top" src="placeholder.jpg" alt="card example image">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Card description goes here.</p>
    <a href="#" class="card-link">Link to somewhere.</a>
  </div>
</div>
```
* Additional card information: https://getbootstrap.com/docs/4.2/components/card/
* Carousel component information: https://getbootstrap.com/docs/4.2/components/carousel/
```
<div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="example_slide_1.png" alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="example_slide_2.png" alt="Second slide">
    </div>
  </div>
</div>
```
* The example above will render a slideshow that loops through two images, displaying one at a time. In the actual code:
	* The parent <div> element has an id of "carouselExampleSlidesOnly", two classes "carousel" and "slide", and the attribute data-ride="carousel".
	* The id is used later when we want to add controls to click between slides.
	* The classes provide the styling and formatting.
	* The data-ride attribute provides the interactivity and slide transitions.
	* We also have a nested <div class="carousel-inner"> element that contains other <div> elements with images.
	* Nested inside the 2nd <div> is yet another <div> with a class of "carousel-item" and "active" (only one image needs the active 	   class, if none have active, no images are shown).
	* Each <div> with .carousel-item has a nested <img> element which have the usual src and alt attributes.
	* The <img> elements use two utility classes"d-block" sets its display as block and the "w-100" is to take up 100% of the width.
