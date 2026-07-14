# Excel Labour Market Analysis Workforce Shortages in Ukraine

## Goal of project
Explore which professions have the greatest shortage of personnel and where does the labor market have an imbalance?
## Data Overview
The dataset contains information about vacancies and jobseekers by profession from January to June 2026.
__Source_: State Employment Service of Ukraine (Diia Open Data)_
There are next columns in the table:
- Profession
- Code of profession
- Number of vacancies (data for Jan - May of 2026)
- Number of jobseekers (data for Jan - May of 2026)
- Jobseekers who had the status of unemployed (data for Jan - May of 2026)
- Number of vacancies (data for June of 2026)
- Number of jobseekers (data for June of 2026)
- Jobseekers who had the status of unemployed (data for June of 2026)
## Data Cleaning (Power Query)
- Identified 4 duplicate records based on Profession and Profession Code. Removed duplicates to prevent double counting during aggregation.
- In profession column text starts with space. Decision is to Trim it.
- The category "People with no profession" contains missing values ("X") in vacancy fields. These values were treated as unavailable data rather than zero.
- Replaced "X" values with null to preserve missing information and avoid incorrect numerical calculations.
- Added new columns for better analyse: Number of seekers for 1 vacancy(for both periods of Jan-May and June), unemployment percentage (for both periods), personnel shortage (for both periods), change of personnel shortage, Change of number of seekers for 1 vacancy (2 columns with percentage and number change values), current status of personnel shortage and status of personnel shortage(trend) (in last 2 columns values strong staff surplus; moderate surplus; balance; moderate deficit; 
strong deficiency added)

_Profession Code was not used as a unique identifier because multiple professions can share the same code._
## Analysis
### Labor Market Supply & Demand Analysis
Peak Job Demand (Maximum Number of Vacancies): Trade and service workers; The simplest professions; Skilled workers with tool; Workers in maintenance, operation and control over the operation of technological equipment, assembly of equipment and machines; Professionals; Specialists

Peak Candidate Supply (Maximum Number of Job Seekers): Trade and service workers; Persons without a profession(not unemplomened, but candidates who are looking for any specific job); The simplest professions; Workers in maintenance, operation and control over the operation of technological equipment, assembly of equipment and machines; Specialists; Professionals; Skilled workers with tool; Legislators, senior civil servants, managers; Technical employees

_Information for both periods of Jan-May and June_

_Insight: Professions with the highest demand (number of vacancies) also attract the largest supply of job seekers_

Competition Level (Job Seekers per Vacancy): 
Jan - May:
Shooter; Machine gunner; Director (Head) of the Small Trading Firm; Philologist; Radiotelephone operator
June:
Shooter; Heater; Machine gunner Branch commander; Seller (On the Market); Radiotelephone operator


_Insight: Most of jobseekers who are looking for job in army professions are unemployed_

