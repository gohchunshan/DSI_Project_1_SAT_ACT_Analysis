<img src="http://imgur.com/1ZcRyrc.png" style="float: left; margin: 20px; height: 55px">

# Project 1: Standardized Test Analysis
For General Assembly DSI Course

## Problem Statement
As an advisor to state governments who have not adopted the use of compulsory or free statewide assessments for SAT or ACT, I am using data-backed evidence to recommend whether there is value for state governments to provide free or compulsory SAT or ACT improve students' scores and chances of getting into a college of their choice.

## Background
The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).


## Choosing Data
For this project, I will be using the following datasets:

The following ACT datasets from 2017 to 2019 describe the Participation rate and Composite Test scores for all 50 US states. The ACT 2017 dataset also contains the individual ACT subjects' test scores.

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State

The following SAT datasets from 2017 to 2019 contain the Participation rate and Subject and Total Test scores for all 50 US states.
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State

The following datasets from the US Census Bureau contain data about the each state such as the spending on education, mean wage etc.
* [`US Census Data`](./data/US Census Bureau.xlsx): containing the following datasets
- a. Median household income of Overall US and all US states from 2017 to 2019
- b. Per Capita Income of Overall and all US states
- c. US Population data with proportion of population with Bachelor's Degree or higher
- d. Each US State's spending per pupil

US Census data obtained from the following source: https://en.wikipedia.org/wiki/List_of_U.S._states_and_territories_by_income (data.census.gov)


## Outside Research

Making standardized testing compulsory and/or free for students has been a trend of state governments.

According to a Los Angeles Times article (https://www.latimes.com/local/education/la-me-edu-lausd-sat-juniors-20190330-story.html), LA had all juniors take the SAT, a standardized college admissions test, on a school day, for free. This increases access to higher education for low-income students. Most four-year colleges require applicants to take either the SAT or the ACT. Experts recommend giving the tests a first try during junior year.


**Below are some of the policies of different states**
(Information from: https://mindfish.com/which-states-require-the-sat/, https://blog.prepscholar.com/which-states-require-the-act-full-list-and-advice)

**The States that Require the SAT**

The following states require high school juniors to take the SAT and offer the test as part of statewide assessments:

- Colorado
- Connecticut
- Delaware
- Illinois
- Michigan
- New Hampshire
- Rhode Island
- West Virginia

**Some states with other arrangements for the SAT**

- The District of Columbia: does not require students to take the SAT but offers the test for free to all juniors and seniors.
- Idaho: offers the SAT through the School Day Test. Juniors are required to take either the SAT or ACT.
- Maine: Taking the SAT is optional for Maine juniors, but the state still offers it to its students for free.
- Tennessee: Students are required to take either the SAT or the ACT.
- Ohio: Students are required to take either the SAT or the ACT. Individual school districts within Ohio can select which test they will give.
- Oklahoma: Students are required to take either the SAT or the ACT, but it varies from school district to school district within the state.
- South Carolina: Students are required to take either the SAT or the ACT, but it varies from school district to school district within the state.

**The States that Require the ACT**
- Alabama
- Hawaii
- Montana
- Nebraska
- Nevada
- North Carolina
- North Dakota
- Wisconsin
- Kentucky (no Writing)
- Louisiana (no Writing)
- Mississippi (no Writing)
- Utah (no Writing)
- Wyoming (no Writing)

**Some states with other arrangements for the ACT**
- Arkansas — offered but not required; no Writing
- Kansas — offered but not required; no Writing
- Minnesota — SAT or ACT offered
- Ohio — SAT or ACT required; district determines which test
- Oklahoma — SAT or ACT required; district determines which test
- South Carolina — SAT or ACT required
- Tennessee — SAT or ACT required (districts may provide either SAT or ACT or allow students to choose)

## Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|	state	|	*object*	|	df_us_sat_act	|	Name of the U.S. state or district	|
|	sat_part_17	|	*float* |	df_us_sat_act	|	SAT 2017 participation rate	(units percent to two decimal places i.e. 1.00 means 100%)|
|	sat_ebrw_17	|*integer*|	df_us_sat_act	|	SAT 2017 Evidence-Based Reading and Writing average score for each state	|
|	sat_math_17	|*integer*|	df_us_sat_act	|	SAT 2017 Math average score for each state	|
|	sat_total_17	|*integer*|	df_us_sat_act	|	SAT 2017 Total average score for each state	|
|	sat_part_18	|	*float*	|	df_us_sat_act	|	SAT 2018 participation rate	(units percent to two decimal places i.e. 1.00 means 100%)|
|	sat_ebrw_18	|*integer*|	df_us_sat_act	|	SAT 2018 Evidence-Based Reading and Writing average score for each state	|
|	sat_math_18	|*integer*|	df_us_sat_act	|	SAT 2018 Math average score for each state	|
|	sat_total_18	|*integer*|	df_us_sat_act	|	SAT 2018 Total average score for each state	|
|	sat_part_19	|	*float*	|	df_us_sat_act	|	SAT 2019 participation rate	(units percent to two decimal places i.e. 1.00 means 100%)|
|	sat_ebrw_19	|*integer*	|	df_us_sat_act	|	SAT 2019 Evidence-Based Reading and Writing average score for each state	|
|	sat_math_19	|*integer*|	df_us_sat_act	|	SAT 2019 Math average score for each state	|
|	sat_total_19	|*integer*|	df_us_sat_act	|	SAT 2019 Total average score for each state	|
|	act_part_17	|	*float*	|	df_us_sat_act	|	ACT 2017 Math average score for each state	(units percent to two decimal places i.e. 1.00 means 100%)|
|	act_eng_17	|	*float*	|	df_us_sat_act	|	ACT 2017 Math average score for each state	|
|	act_math_17	|	*float*	|	df_us_sat_act	|	ACT 2017 Math average score for each state	|
|	act_reading_17	|	*float*	|	df_us_sat_act	|	ACT 2017 Math average score for each state	|
|	act_science_17	|	*float*	|	df_us_sat_act	|	ACT 2017 Math average score for each state	|
|	act_composite_17	|	*float*	|	df_us_sat_act	|	ACT 2017 Math average score for each state	|
|	act_part_18	|	*float* |	df_us_sat_act	|	ACT 2018 participation rate	(units percent to two decimal places i.e. 1.00 means 100%)|
|	act_composite_18	|	*float*	|	df_us_sat_act	|	ACT 2018 average composite score	|
|	act_part_19	|	*float*	|	df_us_sat_act	|	ACT 2019 participation rate	(units percent to two decimal places i.e. 1.00 means 100%)|
|	act_composite_19	|	*float*	|	df_us_sat_act	|	ACT 2019 average composite score	|
|	state_rank	|	object	|	df_us_sat_act	|	State rank of mean household income based on US Census Bureau	|
|	hh_income_17	|*integer*|	df_us_sat_act	|	Mean household income per state in 2017	(units in USD)|
|	hh_income_18	|*integer*|	df_us_sat_act	|	Mean household income per state in 2018	(units in USD)|
|	hh_income_19	|*integer*|	df_us_sat_act	|	Mean household income per state in 2019	(units in USD)|
|	percapita_income	|	*float*	|	df_us_sat_act	|	Mean per capita income in 2020 based on US Census Bureau	|
|	state_pop	|	*float*	|	df_us_sat_act	|	State population 2020 based on US Census Bureau	|
|	no_of_households	|	*float*	|	df_us_sat_act	|	No of households in each state	|
|	pct_highschool	|	*float*	|	df_us_sat_act	|	Percentage of population with at least High school diploma	|
|	pct_bachelors	|	*float*	|	df_us_sat_act	|	Percentage of population with at least Bachelor's degree	|
|	pct_adv_degree	|	*float*	|	df_us_sat_act	|	Percentage of population with an advanced degree and above	|
|	pop_highschool	|*integer*|	df_us_sat_act	|	State population that has at least a High school diploma	|
|	pop_bachelors	|*integer*|	df_us_sat_act	|	State population that has at least a Bachelor's degree	|
|	pop_adv_degree	|*integer*|	df_us_sat_act	|	State population that has an advanced degree and above	|
|	statespending_perpupil	|	*float*	|	df_us_sat_act	|	2020 State spending on education (units in USD)|
|	is_sat_free	|	*boolean*	|	df_us_sat_act	|	Whether SAT is provided free of charge in the state as of 2020 |
|	is_act_free	|	*boolean*	|	df_us_sat_act	|	Whether ACT is provided free of charge in the state as of 2020 |
|	is_sat_required	|	*boolean*	|	df_us_sat_act	|	Whether SAT is required in the state as of 2020 |
|	is_act_required	|	*boolean*	|	df_us_sat_act	|	Whether ACT is required in the state as of 2020 |

## Brief Summary of Analysis

## Conclusions and Recommendations


