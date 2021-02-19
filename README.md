### Overview

For our first project, we're going to take a look at aggregate SAT and ACT scores and participation rates in the United States. We'll seek to identify trends in the data and combine our data analysis with outside research to address our problem statement.

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

---

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|allscore|Name of all 50 states plus District of Columbia|
|sat_participation_2017|float|sat2017|SAT Participation rate in 2017|
|sat_ebrw_2017|int|sat2017|SAT Evidence-Based Reading and Writing score in 2017|
|sat_math_2017|int|sat2017|SAT Math score in 2017|
|sat_total_2017|int|sat2017|Total SAT score in 2017|
|act_participation_2017|float|act2017|ACT Participation rate in 2017|
|act_total_2017|float|act2017|Total ACT score in 2017|
|sat_participation_2018|float|sat2018|SAT Participation rate in 2018|
|sat_ebrw_2018|int|sat2018|SAT Evidence-Based Reading and Writing score in 2018|
|sat_math_2018|int|sat2018|SAT Math score in 2018|
|sat_total_2018|int|sat2018|Total SAT score in 2018|
|act_participation_2018|float|act2018|ACT Participation rate in 2018|
|act_total_2018|float|act2018|Total ACT score in 2018|
|sat_participation_2019|float|sat2019|SAT Participation rate in 2019|
|sat_ebrw_2019|int|sat2019|SAT Evidence-Based Reading and Writing score in 2019|
|sat_math_2019|int|sat2019|SAT Math score in 2019|
|sat_total_2019|int|sat2019|Total SAT score in 2019|
|act_participation_2019|float|act2019|ACT Participation rate in 2019|
|act_total_2019|float|act2019|Total ACT score in 2019|
|sat_parti_change_18(%)|float|allscore|The change in SAT participation rate from 2017 - 2018|
|sat_parti_change_19(%)|float|allscore|The change in SAT participation rate from 2018 - 2019|
|act_parti_change_18(%)|float|allscore|The change in ACT participation rate from 2017 - 2018|
|act_parti_change_19(%)|float|allscore|The change in ACT participation rate from 2018 - 2019|
|sat_parti_change_all(%)|float|allscore|The change in SAT participation rate from 2017 - 2019|
|act_parti_change_all(%)|float|allscore|The change in ACT participation rate from 2017 - 2019|
|region|object|allscore|Identify which region the states are in (Northeast, Midwest, South, West)|

---

### Datasets

I have picked these 6 data sets to explore

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
