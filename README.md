# WebScrapping-Project

Documentation of webscrapping project by Sahil Khimani
Procedure used for web scrapping:
All imports:
We imported BeautifulSoup, pandas, requests, lxml

https://github.com/sahilkhimani/WebScrapping-Project/blob/images/1.png

BeautifulSoup was imported from bs4 library. This package is used for retrieving data from web address.
The requests module allows to send HTTP requests using 
Python. The HTTP request returns a Response Object with all the response data (content, encoding, status, etc).
We use lxml interface with beautifulSoup to parse the data in HTML.
Pandas is a popular Python package for data science, and with good reason: it offers powerful, expressive and flexible data structures that make data manipulation and analysis easy, among many other things. The DataFrame is one of these structures.

Code:




From line 1 to line 4, we have created 4 lists which will become different columns of our csv file.
At line 6, an integer with value 0 is initialized which will become serial number of each row by incrementing at line 13 and on adding to serial list at line 14.
On line 7, a for loop is created of range 110 which will scroll through each page of website one by one. Thus retrieving 100 records per page and a total of approx. 11k row records.
On line 8, a print function is called which will show the page number being processed.
On line 9, a variable ‘url’ is initialized having value of the web address to be scrapped.
On line 10, requests module is used to get the data in text form from the given url.
On line 11, data is parsed to html by using BeautifulSoup library and lxml package.
We inspected the source code of the url by using the f12 key in chrome browser to check the divisions and table structure etc.





At line 12, another for loop is created to retrieve each record present on the current page one by one by calling the table row having attribute ‘itemtype’ = http://schema.org/Book.
At line no 15, a span with attribute ‘itemprop’ =” name” was selected and its text was appended in list ‘name’ at line no 19.
At line no 16, a div with class = “authorName_Container” was selected and its text was appended in list ‘author’ at line no 20.
 At line no 16, a span with class = “minrating” was selected and its text was appended in list ‘rating’ at line no 21.
On line 23 and 24, by using pandas' library all the lists of data are added by column wise into csv file named ‘Books.csv’.

Showing Dataframe:






By using .head() function of dataframe. Few of the records are shown. All records can also be shown on screen.

Showing Dataframe Size:



By using .info() method it is showing the all coulumns name and size of each column.
We have 3 columns and each column have 10900 rows of data.
Book name column has object data type.
Author name column also has object data type.
Ratings column has float data type.
Total memory is using 340.6+ kb.
