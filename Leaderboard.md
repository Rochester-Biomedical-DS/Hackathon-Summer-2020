
<!-- Leaderboard.md is generated from Leaderboard.Rmd. Please edit that file -->

``` r
library(dplyr)
library(drake)
library(readr)
library(ggplot2)
```

``` r
loadd(result_table)
result_table = rowwise(result_table) %>% 
  mutate(score_number = ifelse(is.numeric(scores), scores, Inf), message = ifelse(is.character(scores), scores, ''))
board = result_table %>% arrange(score_number) %>% select(pseudonym, readme_ok, score = score_number, message)
```

# Leaderboard by score

``` r
knitr::kable(board)
```

| pseudonym                                                                                                             | readme\_ok |    score | message                                                      |
| :-------------------------------------------------------------------------------------------------------------------- | :--------- | -------: | :----------------------------------------------------------- |
| Example predictions                                                                                                   | TRUE       | 156.0144 |                                                              |
| Bad repo test                                                                                                         | FALSE      |      Inf | Error in download.file(url, destfile = dest, quiet = TRUE) : |
| cannot open URL ‘<https://raw.githubusercontent.com/amcdavid/Hackathon-Summer-2020/master/prediction/prediction.csv>’ |            |          |                                                              |

*readme\_ok*: was there a README.md publicly available at
github.com/<handle>/Hackathon-Summer-2020? (If FALSE, then the repo
hasn’t been created yet or the handle is incorrect) *score*: Score of
submitted predictions (lower is better). *message*: Error message if
predictions couldn’t be found or
parsed.

# Leaderboard by alphabetical

``` r
knitr::kable(board %>% arrange(pseudonym))
```

| pseudonym                                                                                                             | readme\_ok |    score | message                                                      |
| :-------------------------------------------------------------------------------------------------------------------- | :--------- | -------: | :----------------------------------------------------------- |
| Bad repo test                                                                                                         | FALSE      |      Inf | Error in download.file(url, destfile = dest, quiet = TRUE) : |
| cannot open URL ‘<https://raw.githubusercontent.com/amcdavid/Hackathon-Summer-2020/master/prediction/prediction.csv>’ |            |          |                                                              |
| Example predictions                                                                                                   | TRUE       | 156.0144 |                                                              |
