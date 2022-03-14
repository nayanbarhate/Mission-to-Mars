# Mission-to-Mars
Web scraping methods to extract data using Chrome Developer tools to identify HTML components, Beautiful Soup/Splinter to automate the scrape, MongoDB to store the data, and Flask to display the data.
![astro](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/atstropic.png)

## Overview
The mission with this project was to learn web scraping methods to extract information from the [NASA Science Mars Exploration](https://mars.nasa.gov/) website using `Chrome Developer` tools to identify HTML components, `Beautiful Soup/Splinter` to automate a web browser and perform the scrape, `MongoDB` to store the data, and finally `Flask` to create a web application to display the data. Through the process, the goal was to develop an appt to scrape the following information about the planet Mars:

* Latest News
* Featured Image
* Facts about the planet
* Images of the hemispheres

### Deliverable 1:

To start, we created the file ["Mission_to_Mars_Challenge.ipynb"](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Mission_to_Mars_Challenge.ipynb) in `Jupyter notebook` to perform the scraping activity and pull the requested information needed to build the app. Some of the code used include:

* Visiting the URL `url = 'https://mars.nasa.gov/news/', browser.visit(url)`
* Using `Splinter` and `BeautifulSoup` to automate the browser and parse the HTML element to obtain the latest news title `news_soup = soup(html,'html.parser')`, `slide_elem.find("div",class_='content_title')`, `news_title = slide_elem.find("div", class_='content_title').get_text()`

![ipynb](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/ipynbscreenshot.png)

### Deliverable 2: Update the Web App with Mars’s Hemisphere Images and Titles

Next, we exported our `Jupyter notebook` file into a `Python` [script](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Mission_to_Mars_Challenge.py). Using this script as the starting point, we started to define the scraping process using `Visual Studio Code` to edit our `Python` script. We added functions to scrape through the website(s) and loop through the HTML tags to return the information used to create a database to be stored in `MongoDB`.

![define](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/defineimage.png)

Using the database in `Mongo`, we create a `Flask` app to connect to the information and create our app routes. These [routes](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/app.py) help to display the information on the home page and will perform the scraping of new data using the codes that we wrote in the `Python` script. 

Next, we integrate `Mongo` into the web app so that the data stored is updated every time the script, ["Scraping.py"](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/scraping.py) is run.

After, we create an [HTML template](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/index.html) to customize the the web app and use `Bootstrap` components to enhance the HTML and CSS the file. 

![origjumbo](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/Originjumbotron.png)

Lastly, we modified the HTML file to loop through the dictionary and pull the titles and images for the hemispheres of Mars.

![orighemiphoto](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/originhemiphoto.png)

### Deliverable 3: Add Bootstrap 3 Components

To complete the final deliverable, the following changes were made to the `Bootstrap` components to customize the view of the page:

(1) Updated the color of the Jumbotron header by adding gradient color shading and changing the color of the scrape button.
 - **original tag** `<div class_"jumbotron text-center">` & `<a class="btn btn-primary btn-lg">`
 
 ![jumbotron](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/Originjumbotron.png)

 - **updated tag** `<div style="background:linear-gradient(to bottom, #ffcccc 15%, #e9967a 85%)!important" class="jumbotron text-center">` & `<a class="btn btn-default btn-lg">`
 
![newjumbotron](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/Newjumbotron.png)

(2) Changed the orientation of the hemisphere images to a single ribbon by changing the grid from `col-md-6` to `col-md-3`.

![hemisphere](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/hemisphere.png)

(3) Updated the background color of the entire webpage by modifying the `<body>` tag with `<body style="background-color:darksalmon; color:black">`.

![finalapp](https://github.com/nayanbarhate/Mission-to-Mars/blob/main/Images/MissiontomarsColorchange.png)
