# Overview of Project

This project seeks to visually represent data on High Speed Rail organized by country from the Environmental and Energy Study Institute. This data was sourced from their article "Fact Sheet | High Speed Rail Development Worldwide" by Richard Nunno, 2018[^1]. 

This project occurred to me while reading about petroleum product usage in the United States, in the face of skyrocketing oil costs during the 2022 Russian invasion of Ukraine. As of writing on March 2, 2022, Brent Crude Oil posted a price of $116.77 per barrel. Seeing as the United States is a leader in petroleum consumption, and 45% of US consumption of oil is in the form of automobile gasoline[^2], I became curious about alternative modes of transportation. 

High Speed Rail (HSR) is a fluid term for next generation, long distance, high speed rail transport systems. The article from which this data is derived presents an excellent summary of the history and current state of high speed rail development. When I noticed a table representing various data points about HSR, I became curious to see if this data could be transformed and manipulated. 

My goal became to export this table into Excel for visualization. As my skillset expands to include other data visualization softwares, I may revisit this dataset. 

## Process

My initial attempt at copying and pasting the data resulted in a single column of each string from the table. I recalled that the inspect element of Google Chrome allows a user to see the source code for a webpage. I located the table in the source code. 

![Image 1: Inspect element](https://github.com/ipbrieske/High_Speed_Rail/blob/main/htmlTable.png)

Using VSCode, I was able to isolate and inspect the HTML table in a more managable way. Initially, I attempted to open the code as a CSS file, but VSCode took offense to that. Running the code as HTML created a web document with only the table. The file is included in the repository. 

![Image 2: VSCode](https://github.com/ipbrieske/High_Speed_Rail/blob/main/htmlVscode.png)

From there, I sought to harvest the data from the HTML code. A quick Google search brought me to an HTML to .csv converter, and that gave me the data in a form I was able to open with Excel[^3]. This method did pose a challenge, as the data output held each of the values in the table as strings, confusing Excel's attempts to chart the data. I realized I needed to convert these values into numbers, and that solved the problem. In order to smooth future data harvesting, I researched how to convert HTML tables to .csv files and found it was as simple as taking the code, entering it into a text editor like Notepad, and saving the code as a .xls file. That file is included in the repository and Excel workbook to demonstrate. 

## Results

From the data, I was able to put together three charts to visualize the table in question. The first looks at the sum of all kilometers of track, including length of lines in operation, lines under construction, and lines approved but not started construction. I organized the data this way to get a sense of the overall commitment each country has made to HSR. Using kilometers of track can be a flawed metric, as a country with less surface area would naturally have fewer kilometers of rail service, but this also does color our final analysis, as some countries with relatively small areas like Japan and the United Kingdom have significantly more kilometers laid than larger countries. 

![Image 3: HSRkilometersoftrack](https://github.com/ipbrieske/High_Speed_Rail/blob/main/HSRkilometersoftrack.png)

Clearly, China leads the world in sheer distance. 26,869 kilometers of lines in operation dwarfs the next leading countries, and is a testament to the state's early commitment to investing in an alternative mode of transportation. While usage and quality is not examined in this study, this visualization certainly indicates that at least a large commitment has been made to foster diverse modes of efficient transportation. It goes without saying that shifting energy demand from petroleum to electricity necessitates also using methods of electricity generation that do not rely on pretroleum. France, for example, powers its extensive HSR network with primarily nuclear energy[^4][^5]. 

China's contribution to global HSR was so enormous I found it necessary to examine countries by excluding China.

![Image 4: HSRexChina](https://github.com/ipbrieske/High_Speed_Rail/blob/main/HSRkilometersexChina.png)

Here we see a few countries leading the pack in terms of total kilometers. France, Spain, Japan, and Germany boast extensive systems already, with more under construction. Turkey looks to be a growing force, with countries' worth of kilometers both under construction now and approved. Notably, the United States, Iran, and Indonesia have begun the process of adding to their absent HSR networks, but have yet to make much headway. 

The dataset also included a measure of maximum train speeds, and I've included a ranking of those measurements by country. 

![Image 5: Train Speeds](https://github.com/ipbrieske/High_Speed_Rail/blob/main/MaxSpeed.png)

A relationship exists between the development of a country's rail network and the maximum speed acheived on the network. Speeds of up to 350 km/h begin to rival that of commercial jets, in the 460 - 575 km/h range. HSR shows particular promise as an alternate mode of transport to short range flights. The rail company Brightline aims to expand its rail network into automobile dominated southern California and finally establish rail access between Los Angeles and Las Vegas, alleviating chronic automobile traffic and inefficient "puddle jumper" flights along the route[^6]. 

## Conclusions

This project served as practice converting data between file types, working on independent data research projects, and visualizing data with Excel. I also gained insight into the state of global high speed rail systems, as well as energy generation. I gained experience formatting git text files, and have a pool of data sets to draw from when I need to practice alternative and more complex data visualization tools. 

All in all, petroleum dependence is a matter of global security, not only for the environmental impacts, but because it funds militant autocratic regimes around the world. If automobile transportation is the key contributor to the United States' dependence on petroleum, reducing that consumption in any way is a matter of national security. 


[^1]: Environmental and Energy Study Institute (EESI), “Fact Sheet: High Speed Rail Development Worldwide,” EESI, accessed March 3, 2022, https://www.eesi.org/papers/view/fact-sheet-high-speed-rail-development-worldwide.

[^2]: U.S. Energy Information Administration (EIA), "Oil and petroleum products explained," EIA, accessed March 2, 2022, https://www.eia.gov/energyexplained/oil-and-petroleum-products/use-of-oil.php. 

[^3]: convertcsv.com, "HTML Table to CSV/Excel Converter," accessed March 3, 2022, https://www.convertcsv.com/html-table-to-csv.htm

[^4]: U.S. Energy Information Administration (EIA), "France," accessed March 3, 2022, https://www.iea.org/countries/france. I also included a downloaded .csv file from EIA's website in an Excel sheet with my own graphical confirmation of their data. 

[^5]: Société nationale des chemins de fer français (SCNF), "Leading the charge for a greener planet," accessed March 3, 2022, https://www.sncf.com/en/commitments/sustainble-development/leading-the-charge-for-the-planet#:~:text=The%20transport%20industry%20is%20responsible,for%20moving%20people%20and%20goods. 

[^6]: Brightline, "Brightline West," accessed March 3, 2022, https://www.gobrightline.com/brightline-west. 
