# Project Structure

* /Articles contains the article and codebook pdfs that are referenced in the writing
* /Code contains the cleaning, table & figure generation, and alaysis scripts
* /Figures & /Tables contain the .tex files for each of the tables, all generated by scrips in /Code
* /Writing are the .tex and associated files for the written portions.

DATA CREATED:
We build the _summarized data sets from each of the 5-year teds sets in Clean_Teds.R (Those data sets have to be downloaded seperatley; see .R for more info)

The Pop_ByState are built from the census data

Usage_ByStateYear is the principal data set for this project. It contains the following variables:
- STFIPS and NAME are the states
- YEAR is the year (from ADMYR in TEDS)
- Adm(Alc/Coc/Mar/Her/Opi/PCP/Hal/Ben/NMJ) are the Admissions numbers (from TEDS) for
	- Alcohol, cocaine, marijuana, heroine, opiates, PCP, hallucinogens, benzos, and all non-marijuana admissions
- Rat(Alc/Coc/Mar/Her/Opi/PCP/Hal/Ben/NMJ) are the rate of admissions per 100,000 population (from census state-wide estimates)
	- lRat(Alc/Coc/Mar/Her/Opi/PCP/Hal/Ben/NMJ) are the log(x+1) of the rates. 
	- There are a few (but not many) 0's within the teds data, so the percentage change is approximatley correct in the end results (Wooldridge 2009, p.192)

Data Source:
TEDS: https://www.samhsa.gov/data/data-we-collect/teds-treatment-episode-data-set
2010-2019 Census: https://www.census.gov/data/tables/time-series/demo/popest/2010s-state-detail.html
2000-2009 Census: https://www.census.gov/data/datasets/time-series/demo/popest/intercensal-2000-2010-state.html