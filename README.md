Hello, 

Welcome to our very cool, very awesome **immunity/infection** dataset. Here, we look at 8 lakes every month over the course of a year. We sample the "super"model (credit to Jesse Weber who said this and I found it hilarious), the threespine stickleback, looking for the presence and intensity of infection by the trophically transmitted tapeworm, *Schistocephalus solidus*. Paired with looking into infection dynamics in natural populations we also are able to get a pulse of immune dynamics within these same hosts by the extent of fibrosis present in the peritoneal cavity of fish. How cool is that!

This look a lot of time to wrangle and code, so I am very happy for everyone to look through everything and provide feedback and insight. Thank you for your light and support! 

Shine bright like a tapeworm. Hugz, C.



## Baby fish data sheet
### Variable Definitions

| Variable | Unit | Type | Description | Notes |
|---------|------|------|-------------|-------|
| Lake | — | Factor (8 levels) | Identifier for each lake in the monthly survey | SUG, PCH, SRA, L2B, BEW, FRE, RSS, BLA |
| Mass | grams | Numeric | Fresh mass of individual fish | — |
| Length | mm | Numeric | Standard length of fish | — |
| Total_Worms | count | Integer | Number of tapeworms inside a fish | — |
| CatchDate_clean | day | Date | Year-month-day sampling date | — |
| Season | — | Factor (4 levels) | Season based on sampling month | Summer: Jun–Aug; Fall: Sep–Nov; Winter: Dec–Feb; Spring: Mar–May |
| Month_num | — | Numeric | Sequential month index for sampling | June 2023 = 1 … June 2024 = 13 |
| Month.adj | — | Factor (13 levels) | Each sampling month as distinct factor level | Separate levels for June 2023 and June 2024 |
| Fish_ID | — | Numeric | Unique identifier per fish | Running ID |
| total_worm_wt | grams | Numeric | Total biomass of all worms per fish | — |
| max_worm_wt | grams | Numeric | Biomass of the largest worm per fish | — |

## Fish sizes data sheet
### Variable Definitions

| Variable | Unit | Type | Description | Notes |
|---------|------|------|-------------|-------|
| Lake | — | Factor (8 levels) | Lake identity for monthly survey | SUG, PCH, SRA, L2B, BEW, FRE, RSS, BLA |
| Mass | grams | Numeric | Freshly caught and weighed fish | — |
| Length | mm | Numeric | Standard length of stickleback | — |
| Total_Worms | count | Integer | Number of tapeworms found inside a fish | — |
| CatchDate_clean | day | Date | Sampling date in year-month-day format | — |
| Season | — | Factor (4 levels) | Season classification based on sampling month | Summer = Jun–Aug; Fall = Sep–Nov; Winter = Dec–Feb; Spring = Mar–May |
| Month_num | — | Numeric | Sequential month index for sampling | June 2023 = 1 … June 2024 = 13 |
| Month.adj | — | Factor (13 levels) | Factor identifying each sampling month | Separate levels for June 2023 and June 2024 |
| FishID | — | Numeric | Unique fish identifier as running index | — |
| JOIN_ID | — | Factor | Unique ID to join datasets | Used to merge external .csv files |
| Fibrosis | numeric | Ordinal (0–4) | Fibrosis score per fish | Entered numeric but modeled as an ordinal variable |
| Sex | — | Factor (3 levels) | Sex category of fish | M, F, Juve |
| Schisto_Free | count | Integer | Number of S. solidus freely present in body cavity | — |
| Schisto_cyst | count | Integer | Number of S. solidus encysted in body cavity | — |
| total_worm_wt | grams | Numeric | Total mass of all tapeworms per fish | — |
| ln_wormweight | numeric | Numeric | Natural log of total_worm_wt | — |
| max_worm_wt | grams | Numeric | Mass of the largest tapeworm per fish | — |
| wormbiomass_fishmass | Ratio [0–1] | Numeric | P:H ratio calculated as total_worm_wt / Mass | — |


## Worm weight data sheet
### Variable Definitions

| Variable | Unit | Type | Description | Notes |
|---------|------|------|-------------|-------|
| Date Weighted | Date | D-M-Y | Date on which tapeworms in fish were weighed | Individual worm weights not for baby fish |
|Year | Number | | 2023 or 2024 | — |
| Month_Num | Date | Numeric (1-13) | Numeric version of months starting in July 2023 (1) to July 2024 (13) | — |
| Initials | --| -- | Person who dissected and weighed worms | — |
| Lake | — | Factor (8 levels) | Lake identity for monthly survey | SUG, PCH, SRA, L2B, BEW, FRE, RSS, BLA |
| N_worms_dissected | count | Integer| Number of worms dissected from fish | — |
| N_worms_weighed | count | Integer| Number of worms weighed from fish | — |
| worm_wt_[1..xx]| Numeric | grams| Mass of individiual worm (the _# represents the weight of worm 1, worm2, and so on) | — |
