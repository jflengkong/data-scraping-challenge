# data-scraping-challenge
Week 11 - UWA Data Analytics Web Scraping Challenge 

## Background 
You’re now ready to take on a full web-scraping and data analysis project. You’ve learned to identify HTML elements on a page, identify their id and class attributes, and use this knowledge to extract information via both automated browsing with Splinter and HTML parsing with Beautiful Soup. You’ve also learned to scrape various types of information. These include HTML tables and recurring elements, like multiple news articles on a webpage.

As you work on this Challenge, remember that you’re strengthening the same core skills that you’ve been developing until now: collecting data, organising and storing data, analysing data, and then visually communicating your insights.

## Contents 
1. <b> `Images Folder`</b> : Folder of all images and plot outputs from Jupyter Notebook.
2. <b> `Output Folder` </b> : Folder of [`data.JSON`](https://github.com/jflengkong/data-scraping-challenge/blob/main/Outputs/data.json) and [`Mars_CSV`](https://github.com/jflengkong/data-scraping-challenge/blob/main/Outputs/Mars_Dataframe) file output from Jupyter Notebook
3. [`part_1_mars_news.ipynb`](https://github.com/jflengkong/data-scraping-challenge/blob/main/part_1_mars_news.ipynb) : Scraping of titles and preview texts from Mars News Articles
4. [`part_2_mars_weather.ipynb`](https://github.com/jflengkong/data-scraping-challenge/blob/main/part_2_mars_weather.ipynb) : Scraping and analysis of Mars Weather Data which exists in a table

## Part 1: Web Scraping titles and texts 
The first part of the challenge required us to scrape the titles and preview texts from the [Mars News Site](https://static.bc-edx.com/data/web/mars_news/index.html). By inspecting and analysing which classes, div etc. 
titles to scrape, we stored all news articles into a dictionary into a Python list. 
Optionally, the stored scraped data was exported to a JSON file for ease of sharing the data with others. 

Output Example:

`{'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm", 
 'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}`

 ## Part 2: Web Scraping Mars Weather Data 
 The second part of the challenge required s to scrape the table from the [Mars Temperature Data](https://static.bc-edx.com/data/web/mars_facts/temperature.html) website. 
 With the use of BeautifulSoup and ChromeDevTools we were able to scrape the table. 
 ### Step 1 to 3 
 Visit the website, scrape and store the data into a DataFrame. 

 ### Step 4: Prepare the Data for Analysis. 
 Convert the Data to the appropriate [`datetime`],[`int`], or [`float`] data types. 
 
![Change types](https://github.com/jflengkong/data-scraping-challenge/blob/main/Images/1.%20dtypes.png)

### Step 5: Questions to answer 
Once we were able to sort and complete data scraping, cleaning and sorting, analysis of the dataframe was completed. The following questions were answer through visual and Python analysis. 
1. How many months exist on Mars?
2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?
3. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
    - Find the average minimum daily temperature for all of the months.
    - Plot the results as a bar chart.
  
![sorted_temp](https://github.com/jflengkong/data-scraping-challenge/blob/main/Images/2.sorted_temp.png)

4. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    - Find the average daily atmospheric pressure of all the months.
    - Plot the results as a bar chart.
 
![sorted_pressure](https://github.com/jflengkong/data-scraping-challenge/blob/main/Images/3.sorted_pressure.png)

5. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
    - Consider how many days elapse on Earth in the time that Mars circles the Sun once.
    - Visually estimate the result by plotting the daily minimum temperature.
  
  ![martian_days](https://github.com/jflengkong/data-scraping-challenge/blob/main/Images/4.martian_day.png)
   
#### Analysis and Conclusions 
1. <b>How many months exist on Mars? </b> 
    * There are 12 months on Mars
2. <b>How many Martian (and not Earth) days worth of data exist in the scraped dataset?</b> 
    * There are 1867 Martian days' worth of data in the dataframe provided 
3. <b>What are the coldest and the warmest months on Mars (at the location of Curiosity)?  </b> 
    * The third month has the coldest average temperature on Mars
    * The eighth month has the warmest average temperature in Mars 
4. <b>Which months have the lowest and the highest atmospheric pressure on Mars? </b> 
    * The lowest atmospheric pressure on average is in the sixth month
    * The highest atmospheric pressure on average is in the ninth month 
5. <b>About how many terrestrial (Earth) days exist in a Martian year? </b> 
    * The distance from peak to peak is roughly 1425-750, or 675 days. A year on Mars appears to be about 675 days from the plot. Internet search confirms that a Mars year is equivalent to 687 earth days.
  
## References
[1] Scraping HTML Tables: [SaturnCloud](https://saturncloud.io/blog/how-to-scrape-an-html-table-with-beautiful-soup-into-pandas/) 

[2] Scraping Data Saved into JSON: [StackOverFlow-how-to-save-scraped-data-to-json-in-python](https://stackoverflow.com/questions/71940341/how-to-save-scraped-data-to-json-in-python)

[3] [Mars News Site](https://static.bc-edx.com/data/web/mars_news/index.html) is operated by edX Boot Camps LLC for educational purposes only. The news article titles, summaries, dates, and images were scraped from [NASA's Mars NewsLinks](https://mars.nasa.gov/) to an external site. website in November 2022. Images are used according to the [JPL Image Use Policy](https://www.jpl.nasa.gov/jpl-image-use-policy) to an external site., courtesy NASA/JPL-Caltech. 

