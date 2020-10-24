

Group 2 (super-stars): Members: Sara Simoes, Tyler Brown, Rachel Chan, Kasey (Kassandra) Lacerda

Project Title: Health in Food Deserts Description: Evaluate health status of residents in counties with and without food deserts.
Hypothesis: The presence of a food desert in a county results in decreased health status for residents of that county.

Research Questions:
Do residents of counties with food deserts have reduced health status, as measured by various health factors (e.g. premature death, adult obesity, diabetes)

    Parse data by common characteristic (i.e. county)
    Show food deserts on a heat map (for density)
    Show health status for various health factors on a heat map (for density)
    Overlays:
        premature death and food desert maps
        adult obesity and food desert maps
        premature death and food desert maps
        diabetes and food desert maps
    Comparison of these health parameters in counties with food deserts, versus in counties without.
        Pick representative counties from each group and dive deeper into data
        Pie plots health factor for counties with and without food desert.
        other plots as needed

Bar Graphs:
In order to get valuable data for comparisons I had to take all of the significant population 
based data and normalize it to a percentage. Afterwards, I created a for loop to produce bar graphs based on
each column on a county level. 
I then created another for loop to run comparison bar graphs between food desert population and various health based
parameters accompanied by a quick t-test. Here are the comparisons that probably weren't due to random chance:
    
    Low access pop 1 mile urban - 10 miles rural and medicare percent
    Low access pop 1 mile urban - 10 miles rural and obese percent
    low access pop 1 mile urban - 10 miles rural and %Fair or Poor health

    low access pop 1/2 mile urban - 10 miles rural and medicare percent
    Low access pop 1/2 mile urban - 10 miles rural and obese percent
    Low access pop 1/2 mile urban - 10 miles rural and %Fair or Poor

    Low access pop 1 mile urban - 20 miles rural and medicare percent
    low access pop 1 mile urban - 20 miles rural and %Fair or Poor health

According to the bar graphs, there seems to be a relationship between obesity and the low access populations between
half a mile (urban) from supermarket and 10 miles (rural).
There also seems to be a similar relationship between the fair/poor % and half a mile from supermarkets (urban)
up to 20 miles from supermarkets (rural).
While it isn't due to random chance, we're not entirely sure what the relationship is.

Resources:

    Health Data: https://www.countyhealthrankings.org/explore-health-rankings/rankings-data-documentation/national-data-documentation-2010-2018
    Food Desert Data: https://www.ers.usda.gov/data-products/food-access-research-atlas/download-the-data/
    County Coordinates: https://public.opendatasoft.com/explore/dataset/us-county-boundaries/map/?location=5,69.03242,-35.00244&basemap=jawg.streets
    Medicare Enrollment Data: https://www.cms.gov/Research-Statistics-Data-and-Systems/Statistics-Trends-and-Reports/CMSProgramStatistics/Dashboard
