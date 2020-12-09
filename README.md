# Mission to Mars

![](Images/mission_to_mars.png)

In this assignment, you will build a web application that scrapes various websites for data related to the Mission to Mars and displays the information in a single HTML page. The following outlines what you need to do.

### Step 1 - Scraping

#### NASA Mars News

* Scrape the NASA Mars News Site and collect the latest News Title and Paragraph Text

#### JPL Mars Space Images - Featured Image

* Visit the URL for the JPL Featured Space Image
* Use Splinter to navigate the site and find the image URL for the current Featured Mars Image and assign the URL string to a variable called `featured_image_url`
* Make sure to find the image URL to the full size `.jpg` image
* Make sure to save a complete URL string for this image

#### Mars Facts

* Visit the Mars Facts webpage and use Pandas to scrape the table containing facts about the planet including Diameter, Mass, etc.
* Use Pandas to convert the data to a HTML table string

#### Mars Hemispheres

* Visit the USGS Astrogeology site to obtain high resolution images for each of Mar's hemispheres
* Save both the image URL string for the full resolution hemisphere image, and the Hemisphere title containing the hemisphere name. 
    * Use a Python dictionary to store the data using the keys `img_url` and `title`
* Append the dictionary with the image URL string and the hemisphere title to a list
    * This list will contain one dictionary for each hemisphere

### Step 2 - MongoDB and Flask Application

* Use MongoDB with Flask templating to create a new HTML page that displays all of the information that was scraped from the URLs above
* Convert Jupyter Notebook into a Python Script called `scrape_mars.py` with a function called `scrape` that will execute all of the scraping code from above and return one Python Dictionary containing all of the scraped data
* Create a route called `/scrape` that will import the `scrape_mars.py` script and call the `scrape` function
    * Store the return value in Mongo as a Python Dictionary
* Create a root route `/` that will query the Mongo database and pass the Mars Data into an HTML template to display the data
* Create a template HTML file called `index.html` that will take the Mars Data Dictionary and display all of the data in the appropriate HTML elements

![](Images/final_app_part1.png)

![](Images/final_app_part11.png)



![](Images/final_app_part2.png)

![](Images/final_app_part22.png)

- - -

## Step 3 - Submission

To submit your work to BootCampSpot, create a new GitHub repository and upload the following:

1. The Jupyter Notebook containing the scraping code used.

2. Screenshots of your final application.

3. Submit the link to your new repository to BootCampSpot.

4. Ensure your repository has regular commits (i.e. 20+ commits) and a thorough README.md file

## Hints

* Use Splinter to navigate the sites when needed and BeautifulSoup to help find and parse out the necessary data.

* Use Pymongo for CRUD applications for your database. For this homework, you can simply overwrite the existing document each time the `/scrape` url is visited and new data is obtained.

* Use Bootstrap to structure your HTML template.

### Copyright

Trilogy Education Services © 2020. All Rights Reserved.
