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
