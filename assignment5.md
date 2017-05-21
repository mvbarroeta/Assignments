
# Assignment for week 8

Use the following table to provide us with

|name | exam number|
|----|----|
|Maximilian Tichy|425860|
|M. Victoria Barroeta|933733|
|Magdalena Kuyterink|448037|


In this assignment you will have to make a plot of the mortality due to "Ischemic heart diseases (IHD)". IHD are caused by the
accumulation of fatty deposits lining the inner wall of a coronary artery, restricting blood flow to the heart. IHD alone
were responsible for 644 000 deaths across EU countries in 2013, accounting for around 13% of all deaths. Mortality
rates from IHD are highest in Lithuania, Latvia, the Slovak Republic, Hungary and the Czech Republic, with over 350 deaths per 100 000 population. The countries with the lowest IHD mortality rates are France, Portugal, the
Netherlands, Spain and Belgium. Our plot is taken from http://www.oecd-ilibrary.org/docserver/download/8116231e.pdf?expires=1486219843&id=id&accname=guest&checksum=F326409CF6DCD4DC61990871F943B489 page 63. I have downloaded the data for you and saved it as a csv: mrate.csv.
First read the data with the command read.csv2

If you encounter the problem that all observations per row are in one cell, add: ,sep=";"
The command should look like 
namedf <-read.csv2("name of file", sep=";")


```R
hdata<-read.csv2(file="mrate.csv", head=TRUE,sep=";") 
```

Please have a look at the structure of data with the command str()


```R
str(hdata)
```

    'data.frame':	14 obs. of  7 variables:
     $ Year          : int  2000 2001 2002 2003 2004 2005 2006 2007 2008 2009 ...
     $ Netherlands   : num  158 149 141 135 121 ...
     $ Hungary       : num  417 419 414 440 442 ...
     $ France        : num  94.3 90.7 88 87.1 80.1 77.4 71.2 67.6 64.8 61.2 ...
     $ Lithuania     : num  612 677 666 656 642 ...
     $ United.Kingdom: num  259 250 241 232 213 ...
     $ EU28          : num  221 214 206 205 192 ...
    

Since the data are in the "wide" format, we need to make it in the long format with the package "tidyr". For the graph we need the package ggplot2.

Load the libraries ggplot2 and tidyr with the command library()


```R
library(ggplot2)
library(tidyr)
```

    Warning message:
    "package 'tidyr' was built under R version 3.3.3"

Now we have the most difficult part of the assignment. We need to make a new object and than convert the data in the long format with the command "gather".


The command should look like


new object <- gather(name dataframe, name of the new colum, name of the value, column:column)

* For new object you can use for example p.
* The name of our dataframe was s
* The name of the new column could be Country (since we want the countries to be the observations). Country is a new name.
* The name of the value could be mortality (since the numbers are Age-standardised mortality rates per 100 000 population)
* We need the colums from the Netherlands until EU28 (so you have to fill in Netherlands:EU28).


```R

p <-gather(hdata, Country, mortality, Netherlands:EU28)
```

Now we can make the plot with geom_line of ggplot.
The syntax of the command would be:

ggplot(name of dataframe, aes(x=x-axis, y=y-axis, color=Group)) + geom_line()

* name of dataframe is p if you followed the instructions above (the long format)
* on the x-axis you will need Year
* on the y-axis you will need mortality
* for color you need Country (so we have one line per country)


```R
ggplot(p,aes(x=Year, y=mortality, color=Country))+geom_line()
```




![png](output_11_1.png)



```R

```
