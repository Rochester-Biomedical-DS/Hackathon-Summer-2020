# University of Rochester Biomedical Data Science Hackathon Summer 2020

Data are now live.

# Logistics

0.   Registration is open until 5PM Sunday.  Teams can consist of up to 4 people. Register by using the google form.
1.   You may add team members up
to noon EDT on 8/11 by editing your response to the google form or emailing the organizers.
2.  Teams of entirely undergraduates will be in the undergraduate
division, else they will be in the open division.
3.  Predictions on test data set are submitted by pushing to
    github.  A respository with the name `Hackathon-Summer-2020`,
    owned by the team captain, will
    be queried for a file named [prediction/prediction.csv](prediction/prediction.csv).  **If the team captain forks this
    repository and writes predictions there everything should work
    (as long as the predictions are formatted correctly).**
2.  Predictions will be scored at least once daily, starting 8/8, with
    scores posted by noon.  At
    the organizers' option, predictions may be scored more frequently
    than this.
2.  General questions/problems can be directed to [issues](https://github.com/Rochester-Biomedical-DS/Hackathon-Summer-2020/issues) page.  We encourage other hackathon participants to respond to issues.
3.  The scoreboard is located
    [here](https://rochester-biomedical-ds.github.io/Hackathon-Summer-2020/Leaderboard.html), and will be updated starting noon on 8/8.
    We  cannot provide support
    beyond the diagnostic output included on the scoreboard if an error is
    encountered in scoring your predictions.

# Data

*  Training data are [here](train_data/).  These data include [the labels](train_data/severity_score_train.txt) that you need to predict
*  Test data are here.  Your predictions should be in the order of the `subject_id`s [listed here](prediction/prediction.csv) -- no join is performed on the `subject_id` column.

# Prizes
1.  First place in each division: $300 + $50*(team size)
2.  Second place: 0 + $50*(team size)
3.  In addition, members of teams whose submissions outperform random
    guessing will be entered into a lottery for $20 grubhub
    giftcards.  Up to 30 will be awarded.
1.  Predictions will be scored based on mean square error, lower
values are better.

[**Scoreboard**](https://rochester-biomedical-ds.github.io/Hackathon-Summer-2020/Leaderboard.html)
