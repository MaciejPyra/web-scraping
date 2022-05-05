# Web Scraping

The aim of the project was to develop web scraping tool which is a software program designed specifically to extract (or ‘scrape’) relevant information from internet websites. By making a request to respective URLs my tool is able to find specific data in the HTML. What is important, my program is totally independent of any external website APIs and therefore is very flexible.

Please note that repo includes final source code and two Excels with results of analysis. Each of them provides real data concerning laptop names and their prices - attributes extracted directly from two websites, respectively from www.euro.com.pl and www.komputronik.pl.


# Table of Contents

  * [Introduction](#intro)
     * [What is web scraping?](#intro1)
     * [Data Source](#intro2)
     * [Technology Stack](#intro3)
  * [Program](#desc)
     * [How does it work?](#desc1)


<a name="intro"></a>
<a name="intro1"></a>
## Intorduction
### What is web scraping?

<p align="center">
  <img src="https://github.com/MaciejPyra/web-scraping/blob/main/Web_Scraping.JPG" />
</p>

Web scraping is useful if the public website you want to get data from doesn’t have an API or it does but provides only limited access to the data. Web scraping is the process of collecting structured web data in an automated, programming fashion.

In general, web data extraction is used by people and businesses who want to make use of the vast amount of publicly available web data to make smarter decisions. Unlike the mundane, mind-numbing process of manually extracting data, web scraping uses intelligent automation to retrieve hundreds, millions, or even billions of data points from the internet’s seemingly endless frontier.

<a name="intro2"></a>
### Data Source
My web scraping tool is a program designed specifically to extract relevant information from two chosen websites:
* https://www.euro.com.pl
* https://www.komputronik.pl

They are Polish stores offering, among others computer equipment, household appliances and audio / video devices. In my project I decided to focus only on laptops. My objective was to scrape a lot of different attributes, ranging from the laptop name, through its brand and price, ending with technical characteristics like memory storage, type of processor, disc and screen. 

<a name="intro3"></a>
### Technology Stack
* Python,
* Python HTTP urllib library -> to open URL and get to the website,
* Python BeautifulSoup library -> to parse html and scrape data from the website,
* other popular Python general-purpose programming libraries, like re (regular experession) -> to perform specific subtaks, for example to perform string operations;


<a name="desc"></a>
## Program

<a name="desc1"></a>
### How does it work?
The whole process could be dived into 5 steps:

1. Identify the target website
3. Collect URLs of the pages where you want to extract data from
4. Make a request to these URLs to get the HTML of the page
5. Use locators to find the data in the HTML
6. Save the data in a CSV file

Initially, tool makes HTTP requests respectively to www.euro.com.pl and www.komputronik.pl websites. The scraper loads the entire HTML code for the page in question. Then, received HTML is parsed by BeautifulSoup library and program starts automatic extraction of the interesting data from a given page. After analyzing one specific page, a link to the following one is searched for in its HTML. Thanks to that, tool is self-sufficient and program can jump between pages without user involvement. Finally, the most significant data is saved into a CSV format that is more useful to the end user.
