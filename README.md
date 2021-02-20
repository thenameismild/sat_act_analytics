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

---

### The Analysis

From the selected datasets I will be exploring the trends in SAT and ACT participation rates and their respective total score from 2017, 2018 and 2019.

The total score and the participation rates of each test vary largely from state to state. My goal is to uncover the underlying patterns, to be able to suggest appropriate solutions for the different state to be able to improve their score and their respective prefer test participation rates.

#### The Participation Rates Analysis

Through examing the data set I found that out of the 50 states and District of Columbia, the top states with highest SAT participation rate were: Michigan, Connecticut and Delaware always had 100% participation rate. While the top ACT partipating states were: Mississippi, Iowa, Wisconsin, Wyoming, North Dakota and more had 100% participation rate.

On average around 3 states had 100% participation rate for the SAT and around 17 states had 100% participation rates for the ACT. Over the 3 years there are some shift in participation rates where they increase or decrease over the year. Looking closer in SAT 2017 there were 5 states with 100% participation rate: Connecticut, Delaware, District of Columbia and Michigan. While in ACT 2017 there were 17 states with 100% participation rate: Alabama, Arkansas, Colorado, Kentucky, Louisiana, Minnesota, Mississippi, Missouri, Montana, Nevada, North Carolina, Oklahoma, South Carolina, Tennessee, Utah, Wisconsin and Wyoming.

Over the three years Connecticut, Delaware and Michigan show no changes in full participation for the SAT test. While Alabama, Arkansas, Kentucky, Louisiana, Mississippi, Missouri, Montana, Nevada, North Carolina, Oklahoma, South Carolina, Tennessee, Utah, Wisconsin and Wyoming showed no changed in ACT full participation aswell.

However, from SAT 2017 to SAT 2018 District of Columbia participation rate dropped by 8% and then increase by 2% from 2018 to 2019 SAT testing. Similarly with the ACT where we see that Colorado participation rate dropped by 70% from 2017 to 2018 testing and then droped again by 3% from 2018 to 2019. Another state that saw a change in ACT participation was Minnesota where we saw a decrease by 1% from 2017 to 2018 then another decrease by 4% from 2018 to 2019.

Moving on to looking at full participation in SAT 2018 we see an addition of Idaho that have full participation. While in ACT 2018 we see an addition of states like Nebraska and Ohio who also have a 100% participation rate during the ACT 2018 test.

We see no decrease in the SAT 2018 to 2019 participation. However, there were some changes in the ACT 2018 to 2019 particpation rate where Missouri showed a 18% decreased and South Carolina showed a 22% decrease in participation rate from ACT 2018 to 2019 testing.

The most notable changes were when Colorador ACT participation rate dropped by 70% from 2017 to 2019 and Illinois ACT participation rate dropped by 50% from 2017 to 2018. As you can see there is more fluctuation within the ACT participation rate compare to the SAT this could be becuase of the change in education system in different states or government sponsorship for the different tests.

Eventhough there is alot of varying in the participation rates, the states that have 50% or more participation rates in both test stay constant. These states includes: Florida, Hawaii, Georgia, North Carolina and South Carolina. They all have keep their participation rates above 50% in both test and during consecutive years.

#### The Total Score Analysis

As we explore the toal score, we will be looking at the average score of the SAT and ACT by each state. Looking at the SAT score where its full score is 1600. We see that in 2017 the top 5 states that scored the highest were Minnesota with an average of 1295 followed by Wisconsin at the average of 1291, then Iowa with the average score of 1275, then Missouri with 1271 score and Kansas at 1260. While the bottom 5 for SAT 2017 were Maine with 1012, Idaho and Michigan at 1005, Delaware at 996 and the lowest was District of Columbia at 950 marks.

In SAT 2018 the top 5 states were Minnesota at 1298, followed by Wisonsin at 1294, then North Dakota at 1283, then Iowa and Kansas at 1265. While the lowest 5 were Hawaii at 1010, Idaho at 1001, then West Virginia at 999, Delaware at 998, and at the bottom like SAT 2017 is DIstrict of Columbia at 977 marks.

In SAT 2019 the top 5 states were once aagain like 2017 and 2018 Minnesota(1284), Wisconsin(1283),South Dakota(1268),Noth Dakota(1263) and a new state Nebraska at 1260 marks. While the lowest 5 were also the same states with Idaho(993), Delaware(985), District of Columbia(975), Oklahoma(963), West Virginia(943).

Similarly to the SAT, we are also explorng the top and bottom states average ACT score. The ACT full score is 36 and in 2017 the top 5 states were New Hampshire at 25.5, Massachusetts at 25.4, then Connecticut at 25.2, Maine at 24.3 and District of Columbia at 24.2. While the lowest scoring states were North Carolina at 19.1, then Hawaii at 19, Douth Carolina at 18.7, Mississippi at 18.6 and the lowest scorring state was Nevada at 17.8 marks.

In ACT 2018 the highest scoring state was Connecticut at 25.6 marks, followed by Massachusettes at 25.5 then New Hampshire at 25.1, Neew York at 24.5 and Michigan at 24.2. While the lowest scoring states were Alabama at 19.1, then Hawaii at 18.9, Mississippi at 18.6, South Carolina at 18.3 and Nevada at 17.7 marks.

In ACT 2019 the highest scoring states were similar to past year where Massachusetts and COnnecticut were the highest at 25.5, folowed by New Hampshire at 25, then Rhode ISaland at 24.7 and New York at 24.5. While the lowest socring states were also similar with Alabama at 18.9, South Carolina and Louisiana at 18.8 and at the bottom like the last two years were Mississippi at 18.4 and Nevada at 17.9.

---

### The Solution

