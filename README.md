<<<<<<< HEAD
# CrossFit Data Project


## A Couple notes
### 1. The base url defaults to division = 1 which will return the men's 18-35 data. So there is no need to query any info in the url if you only want the INDIVIDUAL Men's results.

In the examples I used to start you needed the `endpoint_url` and the `main_query` to access the mens open data.

I will only be using Games data. But feel free to check out [reddit](https://www.reddit.com/r/crossfit/comments/129kwir/crossfit_games_api/) for the open url. The article [Analysing the 2019 Crossfit Games using Python](https://medium.com/@arnarhardarson/analysing-the-crossfit-games-2019-with-python-21809a874962) is a great starting point if you want to see a full project on games data.

```python
division = 1
open_endpoint = 'https://c3po.crossfit.com/api/competitions/v2/competitions/open/2023/leaderboards'
open_query = f'?view=0&division={division}&region=0&scaled=0&sort=0'

games_endpoint = 'https://games.crossfit.com/competitions/api/v1/competitions/games/2020/leaderboards'
games_query = f'?division={division}&sort=0&page=1'

```
### 2. The api has changed. If you want to access data past 2020 then the article linked above won't work. `v1` seems to be pre 2021 and `v2` post 2020. Although it seems that `V2` can access the same results as `v1`.
```python

before_2021 = f'https://games.crossfit.com/competitions/api/v1/competitions/games/{year}/leaderboards?division=2&sort=0&page=1

after_2021 = f'https://c3po.crossfit.com/api/competitions/v2/competitions/games/{year}/leaderboards'
```
=======
# Divisions
## Each division is split by gender. You can read them below as Men, Women.

**Individual**
- 1, 2

**Teams**
- 11 

**Age Groups**
- 3, 4 = 45-49
- 5, 6 = 50-54
- 7, 8 = 55-60
- 18, 19 = 35-39
- 12, 13 = 40-44 
- 14, 15 = 14-15
- 16, 17 = 16-17
- 36, 37 = 60-64
- 38, 39 = 65+

## Adaptive

**Upper Extremity**
- 20, 21
  
**Lower Extremity**
- 22, 23
  
**Multi Extremity**
- 24, 25
>>>>>>> 2e9db660deda89ded847f7d909aecd17b2192028
