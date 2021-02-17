### Overview

For our first project, we're going to take a look at aggregate SAT and ACT scores and participation rates in the United States. We'll seek to identify trends in the data and combine our data analysis with outside research to address our problem statement.

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

### Problem Statement

Generally speaking, you will be asked to come up with a data science problem. This problem is ultimately up to you, but below are some guidelines/things to consider when crafting a problem statement:
> 1. Consider your audience. Who is your project going to help? Who will your presentation be geared towards? Establishing your audience first can help you narrow down your scope.
> 2. Consider the data you will use. Based on the contents of this data, think about some questions you could reasonably answer. These questions should aim to solve some kind of problem.
> 3. Based on these questions, what would bring some kind value to your audience? This can be business insights, increase sales, make decisions, etc.
> 4. Put everything from the above steps together into a few sentences that describe the specific problem you are trying to solve and who it will benefit.
> [Here is a blog post](https://towardsdatascience.com/defining-a-data-science-problem-4cbf15a2a461) about crafting a data science problem statement.

Here are some example prompts if you need inspiration:
> * The new format for the SAT was released in March 2016. As an employee of the College Board - the organization that administers the SAT - you are a part of a team that tracks statewide participation and recommends where money is best spent to improve SAT participation rates. Your presentation and report should be geared toward non-technical executives with the College Board and you will use the provided data and outside research to make recommendations about how the College Board might work to increase the participation rate in a *state of your choice*.
> * You work for a school district that has asked you to advise their high school students on what SAT or ACT score they should be aiming for based on their intended area of study or school preferences.
> * You are hired by the state of California to analyze standardized test performance for various districts in the state and identify trends so they can allocate resources appropriately.
> * Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)). You are hired by a college to advise their admissions team on why this should or should not continue beyond the Fall 2021 applications. (Note: problem statements related to this prompt may not be reasonable to answer just using the data provided. If you want to tackle this one, you may need to find additional data online.)
> * *Feel free to be creative with your own prompt!*

And here are some example problem statements related to the above prompts. Come up with your own or modify these for your needs, do not just copy the ones given here:
> * The new format for the SAT was released in March 2016. Since then, levels of participation in multiple states have changed with varying legislative decisions. This project aims to explore trends in SAT and ACT participation for the years 2017-2019 and seeks to identify states that have decreasing SAT participation rates.
> * High school students often know which colleges they would like to consider, but rarely know what SAT or ACT score they should aim for when applying to these colleges. We wish to explore the schools that have the highest and lowest SAT and ACT score requirements and see if there is a relationship between college prestige and test scores.
> * The state of California has many school districts. This project aims to identify the districts that have the worst overall student performance on the SAT and ACT tests so the state can recommend programs and allocate resources to these districts in need.
> * We hypothesize that student performance on these tests is not an indicator of overall academic performance. This project seeks to see if a relationship exists between student GPA and SAT/ACT scores to support or oppose the continuation of these tests as a requirement for college applications.
> * *Feel free to be creative with your own problem statement!*

---

### Datasets

#### Provided Data

There are 10 datasets included in the [`data`](./data/) folder for this project. You are required to pick **at least two** of these to complete your analysis. Feel free to use more than two if you would like, or add other relevant datasets you find online.

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* [`act_2019_ca.csv`](./data/act_2019_ca.csv): 2019 ACT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://www.cde.ca.gov/ds/sp/ai/reclayoutact19.asp))
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State ([source](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/))
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* [`sat_2019_by_intended_college_major.csv`](./data/sat_2019_by_intended_college_major.csv): 2019 SAT Scores by Intended College Major ([source](https://reports.collegeboard.org/pdf/2019-total-group-sat-suite-assessments-annual-report.pdf))
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School ([source](https://www.cde.ca.gov/ds/sp/ai/) | [data dictionary](https://www.cde.ca.gov/ds/sp/ai/reclayoutsat19.asp))
* [`sat_act_by_college.csv`](./data/sat_act_by_college.csv): Ranges of Accepted ACT & SAT Student Scores by Colleges ([source](https://www.compassprep.com/college-profiles/))

**Make sure you cross-reference your data with your data sources to eliminate any data collection or data entry issues.**

#### Additional Data
You are welcome to add any other data sources you find online to support your analysis, but this is **not required**.
