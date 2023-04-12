# mars-challenge

## Mars News

The script performs web scraping on a Mars news site to extract the titles and preview text of the articles. It uses the splinter and BeautifulSoup libraries to automate browsing to the site and parse the HTML, respectively.

First, the script sets up the browser using the Browser function from splinter. Then, it visits the Mars news site using the visit function.

Next, the script creates a BeautifulSoup object from the HTML using the soup function. This object can be used to navigate and search the HTML tree.

The script then extracts the titles and preview text of each news item by finding the appropriate HTML elements using the find_all and find functions of the BeautifulSoup object. For each news item, it creates a dictionary with the title and preview keys and appends it to a list of news items.

Finally, the script prints the list of news items and quits the browser using the quit function.

Overall, this script is a simple and effective way to scrape Mars news articles from a website and extract their titles and preview text.



## Mars Weather 

The goal of this project was to scrape Mars weather data from the Mars Temperature Data Site and analyze it using Pandas. The following steps were taken:

The first step was to visit the Mars Temperature Data Site using automated browsing. The website was successfully visited using the Chrome browser. Beautiful Soup was used to scrape the data in the HTML table. All rows of data were extracted using the find_all() method. The scraped data was assembled into a Pandas DataFrame with columns having the same headings as the table on the website. The column headings were 'id', 'terrestrial_date', 'sol', 'ls', 'month', 'min_temp', and 'pressure'. The data types for each column were examined, and if necessary, the data was cast (or converted) to the appropriate datetime, int, or float data types using Pandas' astype and to_datetime methods.

The dataset was analyzed using Pandas functions to answer the following questions:

    How many months exist on Mars?
    The value_counts() method was used to count the number of months on Mars. A total of ten months were found.

    How many Martian (and not Earth) days worth of data exist in the scraped dataset?
    The nunique() method was used to find the number of Martian (and not Earth) days worth of data in the scraped dataset. A total of 37 Martian days worth of data were found.

    What are the coldest and the warmest months on Mars (at the location of Curiosity)?
    The average minimum daily temperature was calculated for each month using the groupby() method. A bar chart was created to visualize the results.

    Which months have the lowest and the highest atmospheric pressure on Mars?
    The average daily atmospheric pressure for each month was found using the groupby() method. A bar chart was created to visualize the results.

    About how many terrestrial (Earth) days exist in a Martian year?
    The number of Earth days in a Martian year was estimated visually by plotting the daily minimum temperature.