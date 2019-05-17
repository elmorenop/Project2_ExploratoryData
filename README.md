# Project2_ExploratoryData
Fine particulate matter (PM2.5) is an ambient air pollutant for which there is strong evidence that it is harmful to human health. In the United States, the Environmental Protection Agency (EPA) is tasked with setting national ambient air quality standards for fine PM and for tracking the emissions of this pollutant into the atmosphere. Approximatly every 3 years, the EPA releases its database on emissions of PM2.5. This database is known as the National Emissions Inventory (NEI). You can read more information about the NEI at the EPA National Emissions Inventory web site.

For each year and for each type of PM source, the NEI records how many tons of PM2.5 were emitted from that source over the course of the entire year. The data that you will use for this assignment are for 1999, 2002, 2005, and 2008.

Review criterialess 
For each question

Does the plot appear to address the question being asked?
Is the submitted R code appropriate for construction of the submitted plot?
Dataless 
The data for this assignment are available from the course web site as a single zip file:

Data for Peer Assessment [29Mb]
The zip file contains two files:

PM2.5 Emissions Data (\color{red}{\verb|summarySCC_PM25.rds|}summarySCC_PM25.rds): This file contains a data frame with all of the PM2.5 emissions data for 1999, 2002, 2005, and 2008. For each year, the table contains number of tons of PM2.5 emitted from a specific type of source for the entire year. Here are the first few rows.


\color{red}{\verb|fips|}fips: A five-digit number (represented as a string) indicating the U.S. county
\color{red}{\verb|SCC|}SCC: The name of the source as indicated by a digit string (see source code classification table)
\color{red}{\verb|Pollutant|}Pollutant: A string indicating the pollutant
\color{red}{\verb|Emissions|}Emissions: Amount of PM2.5 emitted, in tons
\color{red}{\verb|type|}type: The type of source (point, non-point, on-road, or non-road)
\color{red}{\verb|year|}year: The year of emissions recorded
Source Classification Code Table (\color{red}{\verb|Source_Classification_Code.rds|}Source_Classification_Code.rds): This table provides a mapping from the SCC digit strings in the Emissions table to the actual name of the PM2.5 source. The sources are categorized in a few different ways from more general to more specific and you may choose to explore whatever categories you think are most useful. For example, source “10100101” is known as “Ext Comb /Electric Gen /Anthracite Coal /Pulverized Coal”.

You can read each of the two files using the \color{red}{\verb|readRDS()|}readRDS() function in R. For example, reading in each file can be done with the following code:


as long as each of those files is in your current working directory (check by calling \color{red}{\verb|dir()|}dir() and see if those files are in the listing).

Assignmentless 
The overall goal of this assignment is to explore the National Emissions Inventory database and see what it say about fine particulate matter pollution in the United states over the 10-year period 1999–2008. You may use any R package you want to support your analysis.

Questions
You must address the following questions and tasks in your exploratory analysis. For each question/task you will need to make a single plot. Unless specified, you can use any plotting system in R to make your plot.

Have total emissions from PM2.5 decreased in the United States from 1999 to 2008? Using the base plotting system, make a plot showing the total PM2.5 emission from all sources for each of the years 1999, 2002, 2005, and 2008.
Have total emissions from PM2.5 decreased in the Baltimore City, Maryland (\color{red}{\verb|fips == "24510"|}fips=="24510") from 1999 to 2008? Use the base plotting system to make a plot answering this question.
Of the four types of sources indicated by the \color{red}{\verb|type|}type (point, nonpoint, onroad, nonroad) variable, which of these four sources have seen decreases in emissions from 1999–2008 for Baltimore City? Which have seen increases in emissions from 1999–2008? Use the ggplot2 plotting system to make a plot answer this question.
Across the United States, how have emissions from coal combustion-related sources changed from 1999–2008?
How have emissions from motor vehicle sources changed from 1999–2008 in Baltimore City?
Compare emissions from motor vehicle sources in Baltimore City with emissions from motor vehicle sources in Los Angeles County, California (\color{red}{\verb|fips == "06037"|}fips=="06037"). Which city has seen greater changes over time in motor vehicle emissions?
Making and Submitting Plotsless 
For each plot you should

Construct the plot and save it to a PNG file.
Create a separate R code file (\color{red}{\verb|plot1.R|}plot1.R, \color{red}{\verb|plot2.R|}plot2.R, etc.) that constructs the corresponding plot, i.e. code in plot1.R constructs the plot1.png plot. Your code file should include code for reading the data so that the plot can be fully reproduced. You must also include the code that creates the PNG file. Only include the code for a single plot (i.e. \color{red}{\verb|plot1.R|}plot1.R should only include code for producing \color{red}{\verb|plot1.png|}plot1.png)
Upload the PNG file on the Assignment submission page
Copy and paste the R code from the corresponding R file into the text box at the appropriate point in the peer assessment.
