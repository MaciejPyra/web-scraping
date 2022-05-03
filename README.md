# Web Scraping

The aim of the project was the practical implementation of convolutional neural networks and maximizing the accuracy of their classification in terms of recognizing the age range to which the analyzed people belong. Task was to build the model which would provide reliable indication for assigning individual images of faces to appropriate age groups.

Please note that repo code includes not only final models but also processing steps like a try to understand the whole dataset, image preprocessing and data normalization. Aditionally, there was a comprehensive analysis of the best model in terms of classification accuracy and its potential problems with specific category discrimination.


# Table of Contents

  * [Introduction](#intro)
     * [What is web scraping?](#intro1)
     * [Data Source](#intro2)
     * [Technology Stack](#intro3)
  * [Image Preprocessing](#desc)
     * [How does it work?](#desc1)
     * [Image Resizing](#desc2)
     * [Pixel Normalization](#desc3)
  * [Model Building](#usage)
  * [Evaluation of the best model](#optim)
     * [Architecture](#optim1)
     * [Training Process](#optim2)
     * [Classification Heatmap](#optim3)
     * [Classification Mistakes](#optim4)


<a name="intro"></a>
<a name="intro1"></a>
## Intorduction
### Why convolutional neural network?

Web scraping is useful if the public website you want to get data from doesn’t have an API or it does but provides only limited access to the data. Web scraping is the process of collecting structured web data in an automated, programming fashion.

In general, web data extraction is used by people and businesses who want to make use of the vast amount of publicly available web data to make smarter decisions. Unlike the mundane, mind-numbing process of manually extracting data, web scraping uses intelligent automation to retrieve hundreds, millions, or even billions of data points from the internet’s seemingly endless frontier.

<a name="intro2"></a>
### Data Source
Data was collected by Eran Eidinger, Roee Enbar and Tal Hassner and was presented in the paper "Age and Gender Estimation of Unfiltered Faces" (Institute of Electrical and Electronics Engineers, Princeton University, New York, 2013). The authors collected slighty more than 20 000 photos taken with the iPhone 5 or its newer model. The photos were uploaded by users on various social networks.

<a name="intro3"></a>
### Technology Stack
* Python,
* Python HTTP requests library -> to open URL and get to the website,
* Python BeautifulSoup library -> to scrape data from the website,


<a name="desc"></a>
## Image Preprocessing

<a name="desc1"></a>
### How does it work?
My web scraping tool is a software program that’s designed specifically to extract (or ‘scrape’) relevant information from two chosen websites:
* https://www.euro.com.pl
* https://www.komputronik.pl

They are Polish stores offering, among others computer equipment, household appliances and audio / video devices. In my project I decided to focus only on laptops which are sold by the abovementioned companies on their websites.

Tool makes HTTP requests to a target websites and extracts the data from both pages page.

The figure below shows five photos from each category.

<p align="center">
  <img src="https://github.com/MaciejPyra/Human_Age_Recognition/blob/main/Figures/figure7.jpg" />
</p>
