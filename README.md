# SMU-DataArts_Arts-and-Culture-Employment-During-COVID-19

### Report can be found here: COMING SOON! (Code coming soon)

This repository provides the code used to analyze data from the Current Population Survey from the Census Bureau.

Every month, the U.S. Census Bureau surveys roughly 60,000 households as part of the Current Population Survey (CPS), which provides employment data that the Bureau of Labor Statistics (BLS) uses to analyze the U.S. workforce. The survey allows for analysis of employment status, industry and occupation classifications, race, gender, and disability status, among many [other characteristics](https://www2.census.gov/programs-surveys/cps/datasets/2021/basic/2021_Basic_CPS_Public_Use_Record_Layout_plus_IO_Code_list.txt). The survey also provides the mechanism by which the National Endowment for the Arts fields the [Survey of Public Participation in the Arts](https://www.icpsr.umich.edu/web/NADAC/studies/37138) and the [Arts Basic Survey](https://www.icpsr.umich.edu/web/NADAC/studies/37972).
 
When assessing the employment characteristics in the U.S., the BLS focuses on the [labor force](https://www.bls.gov/cps/definitions.htm#lfconcepts) in its monthly reporting, which includes individuals who are in the civilian, non-institutionalized population, ages 16 and older.  Volunteers are not included as part of the labor force definition. Additionally, the labor force only includes those who are employed, absent from a job (vacation, illness, etc.), on layoff awaiting recall, or actively looking (last 4 weeks) and available for work. 

The CPS defines industries, both for- and non-profit, through the use of North American industry Classification System (NAICS) codes, and for this analysis, NAICS codes associated with the arts and culture sector include:

* [Performing arts companies (7111)](https://www.naics.com/naics-code-description/?code=7111)
* [Promoters of performing arts, sports, and similar events (7113)](https://www.naics.com/naics-code-description/?code=7113)
* [Independent artists, writers, and performers (71151)](https://www.naics.com/naics-code-description/?code=711510)
* [Museums, historical sites, and similar institutions (7121)](https://www.naics.com/naics-code-description/?code=7121)
* [Libraries and Archives (51912)](https://www.naics.com/naics-code-description/?code=519120)

To define artist occupations beyond just the arts and culture industries, the CPS utilizes Standard Occupational Classification (SOC) codes. To align with National Endowment for the Arts’ list of [Artistic Occupations](https://www.arts.gov/impact/research/arts-data-profile-series/adp-1/artists-occupations), this analysis uses the following SOC codes to define the universe of artists:

* Actors (27-2011)
* Announcers (27-3010)
* Architects (17-1010)
* Fine artists, art directors, and animators (27-1010)
* Dancers and choreographers (27-2030)
* Designers (27-1020)
* Other entertainers (27-2099)
* Musicians, singers, and related workers (27-2040)
* Photographers (27-4021)
* Producers and directors (27-2012)
* Writers and authors (27-3043)

While these industry and occupation codes do capture artists and the arts and culture sector, we acknowledge that different approaches for NAICS and SOC code inclusion may exist. We have made our analysis code available in this GitHub repository should others wish to replicate this analysis or create their own using different parameters.

In the section on artist demographic characteristics, we make a comparison to the general demographics of the entire United States. This analysis utilizes data from the Census’ American Community Survey (ACS) 2019 5-year estimates as a complement to the labor force data from the CPS. The Census describes the ACS as follows:

The American Community Survey (ACS) is an ongoing survey that provides data every year -- giving communities the current information they need to plan investments and services. The ACS covers a broad range of topics about social, economic, demographic, and housing characteristics of the U.S. population.

The [5-year estimates](https://www.census.gov/data/developers/data-sets/acs-5year.html) from the ACS are "period" estimates that represent data collected over a period of time. The primary advantage of using multiyear estimates is the increased statistical reliability of the data for less populated areas and small population subgroups. 

The 2019 data is the most recent ACS data released by the Census Bureau, with 2020 data expected to be released in early 2022. This analysis will also reference some data from the 2020 Decennial Census, but only data regarding race and ethnicity has been released to date. For consistency across this portion of the report, the charts utilize data from the 2019 ACS.


## Limitations of the CPS

While is it possible to explore many facets of the employment sector from demographics to wages, occupations to industries, and nationwide analysis to particular states or Core Based Statistical Areas, the size of the CPS survey sample can limit the statistical power of an analysis when the pool of survey responses becomes too small through parsing by many variables.  For example, looking at wages of employed artists within the arts and culture sector in the state of Texas who identify as female would result in such a small sample size that the results would not have statistical validity for generalization. The analysis in this report attempts to balance intricate parsing that maintains validity and generalizability of the results.

In addition to sample size considerations, the CPS methods are updated annually to reflect changes in classification and weighting of survey responses. One of the primary reasons for starting this analysis in January of 2020 is that prior to 2020, the NAICS classifications available in the CPS for arts and culture did not include enough granularity to exclude non-arts and culture items. Other sectors such as spectator sports, gambling industries, and golf courses could not be excluded from the general NAICS code associated with Arts, Entertainment, and Recreation. 

There are also discontinuities that surface between December and January data as the CPS data is re-weighted each January to reflect changes within the population generally. 

Artist information is constrained by two components: SOC definitions of artists as defined by the NEA and CPS limitations in only including occupation codes for those in the labor force. This analysis could be recreated utilizing different SOC codes to define “artists” should the NEA definition be insufficient for certain circumstances. As this study focuses on artistic occupations as captured by the CPS, hobbyists and other non-occupational artists are not included.

And finally, throughout this report, keep in mind that the industry analysis focuses on those in the labor force as defined by the BLS above. This analysis excludes those “not in the labor force” as those respondents are not associated with specific industries in the CPS data.
