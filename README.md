# Homeward Bound: The Reverse Migration of America's Polish Diaspora

This repository contains the supplementary data and code for my Columbia Journalism School master's project, which explores the reversal in migration trends between Poland and the United States. After decades of Poles moving to the U.S. in search of prosperity, the tide has turned with Poland's economic rise now drawing people back.

### Background

Growing up in Poland, I always heard stories about the prosperity waiting for those who made the move to the United States — the American dream across the ocean. A bit closer to home, during my time living in the Netherlands, I encountered Polish immigrants who had moved for work during the communist regime, earning money and sending it back home to a Poland that had less to offer when they left. While we spoke the same language and shared citizenship, my sentiments and experiences could not have felt more different. The Poland I knew was advancing at a racing pace — boosted by EU funds, expanding into future-looking sectors and offering young people opportunities not in any way worse than countries further west. And the American dream my grandparents used to describe seemed to be shattering with every next news headline: gun violence, skyrocketing costs of living, growing hostility toward immigrants, to name a few.

In recent years, these thoughts intensified as foreign headlines confirmed that something about the way Poland is viewed by the rest of the world had changed. The country was gaining traction — its economic growth, the safety foreigners praised while strolling Polish cities and its growing prominence on the global scene. Having moved to the U.S., I wanted to find out what the experiences were of people who once felt Poland had nothing to offer and ended up fleeing it. This migration trend had a long history, dating back to the late nineteenth century — always in the direction out of Poland, so much so that the U.S. became home to the largest Polish diaspora, or Polonia, in the world.

This is how "Homeward Bound" evolved into my master's project. What began as a personal observation was later proven by data. Poland's Central Statistical Office noted an increase in Polish citizens returning from abroad and growing interest among foreigners in taking jobs in the country. At the same time, the U.S. recorded net emigration for the first time since the Great Depression. A dozen interviews with Polish Americans and members of the Polish diaspora revealed the human struggles and reflections behind these numbers.

I started my reporting local, finding a place nearby where I could get to know a community that bore the mark of this shift. That led me to Greenpoint, a neighborhood in Brooklyn known for its high concentration of Polish residents. The neighborhood experienced its own version of a Polish exodus driven by gentrification.

### What's in this repository

`thesis_data_analysis.ipynb` documents every data source and analysis step behind the project's two data components:

1. A check of whether the reverse-migration trend I was reporting on is actually supported by migration statistics (UN DESA's bilateral migrant stock data, comparing Americans living in Poland against Poles living in the US, 1990–2024).
2. A mapped, address-level record of Polish business presence and disappearance along Manhattan Avenue, Greenpoint's main commercial corridor, comparing 2007 to today.

### Data sources

- **NYC Planning — Neighborhood Tabulation Areas**: official neighborhood boundaries, used to define Greenpoint precisely.
- **NYC Planning — LION**: the city's street centerline file, used to get Manhattan Avenue's geometry.
- **NYC Planning — MapPLUTO**: tax lot data, used to generate a verified list of every building fronting Manhattan Avenue.
- **UN DESA — International Migrant Stock (2024 edition)**: bilateral migration data by country and sex, used to check the reverse-migration trend against real numbers.
- **Google Street View**: manually reviewed, 2007 vs. present day, to identify Polish businesses along the corridor.

### Methodology notes

The business analysis only included storefronts and did not account for businesses that could have been located on upper floors. It focuses on the existence of Polish businesses and their immediate visibility, not building ownership.

I initially planned to identify historical Polish businesses using the city's 1940s and 1980s tax photo archives (1940s.nyc and 80s.nyc), but this approach proved unworkable — the 1980s photos were too blurred to read most storefront signage and the 1940s photos showed essentially no Polish businesses yet on the corridor. Instead, I compared Google Street View imagery from 2007, the earliest year with consistent coverage of the area, against the present day for each address. I noted which storefronts were Polish-owned in 2007, whether and when they closed and what has replaced them. Often some of the identified storefronts included Polish signage which was later rebranded to only its English version. 

Sixteen addresses were added manually after the Street View review — these were businesses I identified by "walking" the street in Street View that never showed up in the automated, PLUTO-derived address list. In these cases, the city's property records list only one official address per building lot, but several buildings along the corridor have more than one storefront, each with its own separate street number for business signage. Since these separate storefront numbers were never recorded as distinct addresses in city data, they only surfaced through direct visual inspection of the street, not the automated address list. 
