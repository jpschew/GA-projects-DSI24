## Project 1: SAT & ACT Analysis


Students in the United States(U.S) either take the ACT or SAT as a requirement for college admission. Participation rate(%) in the SAT across states are not uniform. Through analysis of SAT historical data, this project aims to provide insights and recommendation for the College Board on improving SAT participation (%).

## Summary of Findings and Recommendation

1)  The participation rate for SAT had an inverse relationship with the particition rate of ACT. It is obeserved that there is a trend in the small shift from ACT to SAT due to the change in policy in having mandatory SAT for college admissions particularly in two states namely Colorado and Illinois.

2) With the dataset, the probability of state with above average SAT participation rate given that the state had a below average ACT participation gave a probability of 0.95 and 0.96 in 2017 and 2018 respectively. Hence, the focus would be to persuade the students from the 9 states that has a slightly below average ACT participation rate. These 9 states include California, Georgia, Indiana, Maryland, Oregon, Texas, Vermont, Virginia snd Washington.

3) With the above observation and analysis, recommended that the resources should focus on the 9 states that have a slightly below average ACT participation rate where the College Board can have an agreement with the 9 states to have SAT mandatory for their college admissions.

---

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|ACT/SAT|State name| 
|part_act_2017|float|ACT|Normalized participation rate for ACT 2017| 
|english_act_2017|float|ACT|Average English score for ACT 2017| 
|math_act_2017|float|ACT|Average Math score for ACT 2017| 
|reading_act_2017|float|ACT|Average Reading score for ACT 2017| 
|science_act_2017|float|ACT|Average Science score for ACT 2017| 
|composite_act_2017|float|ACT|Average Composite score for ACT 2017| 
|part_act_2018|float|ACT|Normalized participation rate for ACT 2018| 
|english_act_2018|float|ACT|Average English score for ACT 2018| 
|math_act_2018|float|ACT|Average Math score for ACT 2018| 
|reading_act_2018|float|ACT|Average Reading score for ACT 2018| 
|science_act_2018|float|ACT|Average Science score for ACT 2018| 
|composite_act_2018|float|ACT|Average Composite score for ACT 2018|
|part_sat_2017|float|SAT|Normalized participation rate for SAT 2017| 
|erw_sat_2017|int|SAT|Average Evidence-based Reading and Writing score for SAT 2017| 
|math_sat_2017|int|SAT|Average Math score for SAT 2017| 
|total_sat_2017|int|SAT|Average Total score for SAT 2017|
|part_sat_2018|float|SAT|Normalized participation rate for SAT 2018| 
|erw_sat_2018|int|SAT|Average Evidence-based Reading and Writing score for SAT 2018| 
|math_sat_2018|int|SAT|Average Math score for SAT 2018| 
|total_sat_2018|int|SAT|Average Total score for SAT 2018|

---
