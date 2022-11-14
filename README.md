# Final-Project-Tableau

## Project/Goals
The goal of this project is to use explore data with Tableau, and find and display meaningful correlations.

## Process
1)  Connect Data
    -   Connected the [TB Burden by Country CSV](https://drive.google.com/file/d/1mRvMbGLzeYKCuELODUhbLYSXM-n6fbQ_/view) to Tableau
2)  Detect Different Data Types
    -   The main data types were numerical data (population numbers, mortalities, incidence rates, etc), along with some geographical data (country names, ISO country codes). Region, while technically a string, was tied to the geographic data.
    -   The methods of collecting data were also all strings
    -   Initially, Year was defined as a number, so I converted it to a year.
3)  Build Visualizations To Learn About The Dataset
    -   Since there was lots of population and geographic data, I built several maps to look for correlations between regions/countries, and tuberculosis rates
        -   I imported a different dataset that used different region classification, to see how that effected the look of any maps
    -   I also made line graphs comparing data to the year, to view how different factors had changed over time
    -   While exploring data, I noticed that some data collecting methods were mistakenly labelled as 'High Income', which made me curious about income data for these countries.
        -   Using World Bank data, I constructed a simple dataset containing countries, and their income group classification by year, and also connected that to my data
3)  Identify The Most Important Features of the Data
    -   Population, geographic location (country and region), year, estimated mortalities (both including and excluding HIV), estimated prevalence, as well as the variations of those numbers per 100 000 people, all felt very important. As did the income classification data that I included.
        -   This data all showed relevance to each other in some way or another
        -   For the purpose of this exploration, I left out the high and low groupings, as they may have lead to comparisons of too many variables
    -   I wanted to explore the relationships between these features, and see if they were correlated in any way.
        -   How does TB prevalence relate to time?
        -   How have mortality rates changed?
            -   How have mortality rates in HIV changed?
        -   Is there a correlation between income and tuberculosis
        -   Does income have any correlation?
4)  Find Interesting Patterns, Trends, Outliers, Etc
    -   China and India were both outliers in population. I had to exclude their data from some maps, and manipulate the data in others, in order for data from other countries to be visible
        -   I did not exclude their data completely, however, as they still represented the lives and deaths of millions of people
    -   Predictably, the prevalence of tuberculosis overall, has lowered over time
    -   Higher income countries tended to have a lower estimate of tuberculosis prevalence
5)  Detect Keypoints
    -   Tuberculosis prevalence has decreased, while case detection rates have increased
    -   Mortality rates have decreased over time, with a notable jump in 2002
    -   Poorer countries, especially those in Africa, have higher prevalence and higher mortality rates
    -   More populated countries have higher rates of tuberculosis
8)  Come Up With Meaningful Questions
    1)  How Has Tb Prevalence Changed Over Time?
    2)  How Have Mortality Rates Changed?
    3)  Does Income Effect TB Rates?
    4)  Are Highly Populated Countries More Susceptible to TB?
9)  Create A Dashboard Addressing These Questions
    -   I created a separate dashboard for each question, as each had multiple factors
    1) How Has Tb Prevalence Changed Over Time? 
        -   I made a line graph comparing the estimated prevalence of tuberculosis, over time, with a forecast for the future. 
        -   I also made a line graph showing the case detection rate over time
    2)  How Have Mortality Rates Changed?
        -   I made a bar graph comparing total mortalities of people with HIV vs those who did not, as well as a line graph showing how this changed over time
        -   I made a box plot showing these same results, in order to get a better idea of these outliers
        -   I clustered these outliers and showed them on a map
    3)  Does Income Effect TB Rates?
        -   I created two maps, one showing World Bank income group classification, and the other showing those same countries grouped by their prevalence of TB per 100,000 people (sorted by percentiles).
        -   I also showed a heat map that of income groups vs average prevalence of TB.
    4)  Are Highly Populated Countries More Susceptible to TB?
        -   I made a linear regression showing tuberculosis prevalence vs population
        -   I also made two maps showing this data separately.


## Results
-   As mentioned above, I went with option 2, and chose the TB World Burden Dataset
-   I created quite a few visualizations with maps, as I felt as though they were the best way to display the differences of TB rates by country or region
    -   I experimented in making other kinds of visualizations using general region classifications, but showing specific countries on a map felt more impactful
-   Since quite a lot of my data involved time, I also used several line graphs. While they are less exciting visually, they are an efficient way to show how data has changed over time
-   When it came to showing total mortality rates over time, I felt like using a box plot was the best way to visually show how important the many 'outliers' in this data are
    -   The box plot, alongside the map showing the same data, shows just how significant these outliers truly are. We can see that even though fewer countries experience these higher rates of mortality, the numbers are still devastatingly high.
-   I found that lots of my data required context from outside of the dataset. In my second question, I saw that there was a peak in mortalities in 2002, so I looked into this further and found out that 2002 was the year that South Africa (a country hit incredibly hard by both Tuberculosis and HIV) lifted certain restrictions on HIV medication. 
-   Something very interesting that I found, was a good example of how predictive modelling can only go so far. I compared my data of TB prevalence over time (with a forecast showing data up to 2020), with the same data from the World Bank. While they had some minor differences, they showed the same downward trend.
    -   My forecast was technically accurate, however, while it showed a downward trend, we know for a fact that in 2021, TB rates increased due to factors related to Covid-19. This felt important to note, as it shows that no matter how accurate our modelling may be, it can never be 100%, simply due to the chaotic and unpredictable nature of our world.

## Challenges 
-   This dataset had an overwhelming amount of factors to choose from, and it was hard to narrow it down. Since so much of this related illness and mortality, it was difficult choosing what to exclude, as it felt disrespectful to treat someone's life as a statistical error
-   It was also difficult to remain focused on specific data and questions, as it was very easy to get lost in a black hole of data exploration

## Future Goals
-   With more time, I would have spent a larger amount of time on examining and cleaning data. As the purpose of this project was focused more on data visualization, I concentrated on finding relationships that could be represented visually
-   I would have liked to combine this with more datasets that included different factors, such as healthcare spending, GDP, etc. The data included was all very broad, and it would be interesting to inspect correlations on more of a micro level

## Sources
-   [Our World In Data Population Density Map](https://ourworldindata.org/grapher/population-density?time=2005)
-   [Country Mapping - ISO, Continent, Region Dataset](https://www.kaggle.com/datasets/andradaolteanu/country-mapping-iso-continent-region)
-   [World Bank Country and Lending Groups](https://datahelpdesk.worldbank.org/knowledgebase/articles/906519-world-bank-country-and-lending-groups)
