# Global Economic Trends (1960 - 2014)

## User Instructions
For a brief outline of the most significant results from the investigation, read the [Summary Document](https://github.com/dilraj451/WDI-Analysis/blob/main/summary_document.pdf).

The data set used in this project was a database stored as a SQLite file. Due to the large file size (> 1GB), the database could not be uploaded to GitHub. To execute the Jupyter Notebook scripts (optional), download the [indicators.sqlite](https://www.kaggle.com/datasets/psycon/world-development-indicators/download?datasetVersionNumber=21) file publicly available on Kaggle and are valid under the Creative Commons Attribution 4.0 International License, as stated by the World Bank.

## Objective
The primary motivation of this project was to uncover any economic trends of interest. During the initial exploratory data analysis, the rapid economic development of newly industrialized countries (NICs) was particularly intriguing and the causes/effects of their development was the focus of the remaining exploration

## Methodology
The project was split into two components: data cleaning and data analysis

Data cleaning (see the [Cleaning Jupyter Notebook](https://github.com/dilraj451/WDI-Analysis/blob/main/cleaning.ipynb)) involved probing the SQLite database using the SQLite3 module to execute queries with purpose of:

* Determining redundant tables in the database
* Cleaning the data stored in necessary tables (i.e. filling blank fields, ensuring correct data formatting, and removing duplicates)

Data analysis (see the [Analysis Jupyter Notebook](https://github.com/dilraj451/WDI-Analysis/blob/main/analysis.ipynb)) involved examining any pertintent economic trends using the plotly module for data vizualization. The primary economic indicators utilised were GDP and Annual GDP Percentage Growth because these are generally correlated with important economic indicators, such as economic output and employment rate. As mentioned, the potential causes of the rapid development of NICs was of particular interest and probed by examining the effects of foreign investment, economic output of different sectors, and the working population upon economic growth.

## Conclusions
* From the 2014 data (latest year included), there is a negative correlation between the country's income (per capita) and the rate of GDP growth on average.

* Higher income countries were more adversely affected (i.e. larger decrease in GDP) during the 2008 global financial crisis.

* Three of the Top 10 Highest-GDP countries (2014) are not classed as high income countries: Brazil, China, and India. These three are the only newly industrialized countries (NICs) in the top 10, and the differences in economic strength and development, between each other and the rest of the world, were examined:
    * Brazil's GDP growth has greater than all other groups during the 1960s and 70s; from the 1980s onwards, China followed by India have much higher GDP growth than the others

    * Strong evidence of a linear correlation between foreign investment and GDP growth in China, Brazil, and the Rest of the Top 10, particularly China where a spike in foreign investment (% of GDP) in 1992-94 coincided with the initiation of exponential GDP growth since then.

    * The relatively low significance of the services sector to the economies of China and India (compared with the Rest of the Top 10) is likely a contributing factor to the much smaller impact the 2008 financial crisis had upon their economies; in fact, both countries experinced GDP growth.
    
    * Clear evidence of a linear correlation between the working age population and GDP growth in China, Brazil, and the Rest of the Top 10; however, the linear correlation coefficeint for the Rest of the Top 10 data is significantly greater than that of China or Brazil, indicating that greater economic value per worker in the Rest of the Top 10.
