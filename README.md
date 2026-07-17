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

| Metric | January-May | June |
|--------|-------------|------|
| Vacancies | 417,509 | 122,706 |
| Job seekers | 632,583 | 266,476 |
| Competition ratio | 1.57 | 1,25 |
| Unemployment seekers | 394,052 | 186,865 |

<img width="1282" height="566" alt="image" src="https://github.com/user-attachments/assets/b2b41d82-f1b6-4005-8761-11752e466e43" />

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
Peak Job Demand (Maximum Number of Vacancies): 
The highest number of vacancies is concentrated in broad occupational groups, primarily:
- Trade and service workers
- Elementary occupations
- Skilled workers with tools
- Machine operators and assemblers
- Professionals and specialists

Peak Candidate Supply (Maximum Number of Job Seekers): 
The largest number of job seekers is observed in similar occupational groups:
- Trade and service workers
- Individuals without a specific profession
- Elementary occupations
- Machine operators and assemblers
- Professionals and specialists

Additionally, higher-level roles such as managers and technical staff also show notable candidate supply.

_Information for both periods of Jan-May and June_

_Insight: Professions with the highest demand (number of vacancies) also attract the largest supply of job seekers_

Competition Level (Job Seekers per Vacancy): 
The highest competition levels are consistently observed in a small group of professions across both periods.

January–May: dominated by military and specialized roles
June: similar pattern, with military-related and low-barrier entry jobs remaining highly competitive

_Insight: Military-related professions demonstrate the highest competition level, with a large number of job seekers competing for available vacancies._

<img width="1514" height="753" alt="image" src="https://github.com/user-attachments/assets/2ad99865-27de-430d-aebb-78d8f3868130" />

### Labour shortage analys
The greatest labour shortage in occupations such as:
Jan - May:
- Skilled Workers With Tool;
- Motor Vehicle Driver;
- Trucker;
- Janitor;
- Barista

June:
- Skilled Workers With Tool;
- Trucker;
- Electrical fitter for repair and maintenance of electrical equipment;
- Locksmith-Plumber;
- Electric gas welder

_Insight: In occupations with the highest labor shortages (high vacancy volume), a large share of job seekers are unemployed, often exceeding 50%. This indicates that despite strong demand, available candidates are not being absorbed into the labor market. This imbalance suggests a mismatch between labor supply and demand, where the presence of job seekers does not translate into successful employment._

Labor oversupply is most evident in large occupational groups such as:
- Trade and service sector employees
- Elementary occupations
- Specialists and professionals
- Administrative and technical staff
- Managers and senior officials

Labor Market Dynamics: Supply–Demand Balance and Trends (Jan-May and June analys)

Most professions are formally in the balance zone, but a large part has a low volume of vacancies. The biggest imbalances are concentrated in professions with a high number of vacancies and a large number of candidates

The next professions may show imbalance:
- Motor Vehicle Driver, Kitchen Worker, Stacker-Packer, Administrator, Landscaping worker, Watchman, Junior Medical Sister, Elementary occupations, Cleaning worker of the Service Premises - high risk of oversupply
- Technician, Economist From Financial Work, Head of the Department, Stormtrooper, Economist, Teacher - high risk of deficit

<img width="1423" height="732" alt="image" src="https://github.com/user-attachments/assets/56af0d37-4fcf-4c7f-8d38-3840717c613b" />

## Key Findings

- The Ukrainian labor market demonstrates a significant imbalance between labor supply and demand. While some professions experience a shortage of workers, many occupational groups have an oversupply of candidates, indicating that the availability of job seekers does not always match the needs of employers.

- The highest demand is concentrated in skilled manual professions, drivers, machine operators, and technical occupations. These roles consistently show a large number of vacancies and remain among the most difficult positions to fill.

- Military-related professions demonstrate one of the highest levels of competition among job seekers. Despite high demand for these occupations, they also have a large number of unemployed candidates searching for these positions. This may indicate that the presence of available candidates does not necessarily translate into successful employment due to possible requirements mismatch, limited available positions, qualification requirements, or other labor market barriers.

- Professions with the highest number of vacancies often also have a significant number of unemployed job seekers. This suggests that the main labor market issue is not only a lack of candidates, but also a mismatch between employer requirements and available workforce skills.

- Large occupational groups such as trade and service workers, elementary occupations, specialists, and administrative roles show signs of candidate oversupply. A high number of job seekers in these areas creates increased competition and may reduce the ability of candidates to find employment quickly.

- The transition analysis between labor market states shows that many professions move from balance toward oversupply, which indicates increasing competition among candidates in certain segments of the market.

- Improving employment outcomes requires not only increasing the number of available workers but also reducing the gap between employer expectations and candidate skills through professional training, reskilling programs, and better alignment between education and labor market needs.
