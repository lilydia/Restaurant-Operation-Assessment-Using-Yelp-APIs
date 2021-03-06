# Restaurant Operation Assessment Using Yelp APIs

# TorontoAftertheFirstWave Applications
> Please note that this project is part of an ongoing project assessing impacts of COVID-19 in Toronto (https://torontoafterthefirstwave.com/). Datasets are collected from Yelp in May 2020, November 2020, and May 2021.
* View Dashboard: https://torontoafterthefirstwave.com/dashboards/restaurants/

## Media Mentions
<!-- toc -->
* [Spacing Toronto Magazine](http://spacing.ca/toronto/2021/04/29/toronto-after-the-1st-wave-how-covid-19-affected-three-key-markets/)
* [University of Toronto Magazine](https://magazine.utoronto.ca/research-ideas/culture-society/the-surprising-resilience-of-restaurants-toronto-covid19-pandemic/)
* [The Global and Mail](https://www.theglobeandmail.com/business/article-the-restaurant-industry-is-hurting-thats-not-stopping-these/)
* [Toronto Star Podcast](https://www.thestar.com/podcasts/thismatters/2021/06/04/how-some-restaurants-opened-and-adapted-during-the-pandemic-and-whats-next.html)
* [Toronto Star News](https://www.thestar.com/news/gta/2021/05/27/pizzas-burgers-sandwiches-more-of-these-restaurants-opened-during-the-pandemic-will-the-trend-continue.html)

# Sampling Method
## First Assessment (May 2020 - November 2020)
Using `SQL EXCEPT` and `SQL INTERSECT`, operation statuses are differentiated into "Open", "New", and "Closed" by comparing datasets collected in May 2020 and November 2020:
![alt text](https://github.com/lilydia/Restaurant-Operation-Assessment-Using-Yelp-APIs/blob/main/images/May2020-Nov2020_Assessment.PNG)

## Second Assessment (May 2020 - May 2021)
By taking the aggregated data from previous assessment, we differentiated more cases:
![alt text](https://github.com/lilydia/Restaurant-Operation-Assessment-Using-Yelp-APIs/blob/main/images/May2020-May2021_Assessment.PNG)
where 
| Case Letter | 2020 Dataset | 2021 Dataset | Description |
| :---: | :---: | :---: | :---: |
| a | New | Found | New - Newly opened between May 2020 and November 2020, and continued to be open in May 20210 |
| b | New | !Found | Closed - Newly opened between May 2020 and November 2020, and closed by May 2021 |
| c | Open | Found | Open - Open before May 2020 and continued to be open in May 2021 |
| d | Open | !Found | Closed - Open before May 2020 and continued to be open until November 2020 and closed before May 2021 |
| e | Closed | Found | Open - Open between May 2020 and November 2020, closed in November 2020, open again in May 2021 |
| f | Closed | !Found | Closed - Open in May 2020 and closed in November 2020 and still closed in May 2021 |
| g | N/A | Found | New - Newly opened between November 2020 and May 2021 |

## Credits
Dataset from May 2020 is sourced from [Kevin Bi](https://github.com/Kevin-Bi/toronto_food_proj?fbclid=IwAR0luS3ea0fHaXQnApMp31geQbZJtFh-4F9t9jt6drb-ICQV9dGH36zxwbg)
