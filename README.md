I created this webapp in order to get familiarized with ReactJS, as well as Bootstrap. For the creation of the chart, I also used [amCharts](https://www.amcharts.com/), a data visualization library. 

This webapp lets the user see the latest price evolution of a cryptocurrency of the user's choice, expressed in terms of another currency, using a zoomable line graph. It has two pages, each of which provides usage instructions.

The first page allows you to choose both the cryptocurrency and the other currency, from two rather lengthy drop-down lists, as well as to set how many days of this cryptocurrency value's latest evolution you would like to see (from how many days ago until the present time). 

After you hit the "Create Chart" button, the app loads the second page, where you can see a line chart that shows the chosen cryptocurrency's value throughout the selected time span. 

The graph can be zoomed to show a shorter time span than the one selected through the first page. On laptop and desktop computers, this can be done by hovering the mouse pointer on the fragment you want to zoom into, while holding the mouse's left button. On a smartphone or a tablet, you can double-tap the screen and drag your finger until the end of the segment of your choice. If you want to zoom back out, there is a button to do so in the chart's  upper-right corner.

Each UI element is encapsulated in its own RectJS component, which in turn is housed in its own `.js` file. For instance, the header shown in both pages, the usage instructions on the first page and the input form and the graph of the second page, are all ReactJS components.

The `Form.js` file contains the form component. It includes the form elements, such as the drop-down menus, input and submit button, as well as the functionality that builds these elements. It also includes the form's events.

The `Graphic.js` file shows the line graph, built with the amCharts library. Of course, it includes the chart related functionality, like the "translation" of the query's data into a line chart itself, the ordering of the data points, for the chart to be created properly, and a few line chart layout settings, such as the color and thickness of the chart's line, the zoom-out button's color, etc. 

The App.js file controls which components are shown in each case, and makes the REST API queries necessary for the creation of the drop-down menus. The API query used to create the chart is housed in `helpers.js`.

The app's layout is created using several Bootstrap classes, as well as the custom CSS rules in the index.css file.


