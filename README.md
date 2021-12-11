# An Analysis of Kickstarter Campaigns
Helping determine trends for a theater client
# Kickstarting with Excel


## Overview of Project
Success isn’t always a measure of talent: it also has much to do with timing. This project seeks to find the optimal timing for the talent of Louise to use crowdfunding to produce her project. Kickstarter [recommends a campaign time of 30 days or less](https://help.kickstarter.com/hc/en-us/articles/115005128434-What-is-the-maximum-project-duration-#:~:text=Projects%20on%20Kickstarter%20can%20last,at%2030%20days%20or%20less.) to reach a funding goal, so timing is very important (no campaigns longer than 60 days are allowed). 


Another important factor in a successful campaign is selecting the right level of funding to seek. No doubt some levels of funding will be easier than others to reach, and I want to help Louise identify a target range of support that is both achievable and will help her produce the play the way she wants.


### Purpose
My analysis will glean data from over 4,000 previous Kickstarter campaigns and provide Louise with two recommendations: what kind of a goal to set, and when to launch her funding campaign.


## Analysis and Challenges
We analyzed over 4,000 previous Kickstarter campaigns, dating from 2009 to 2017. Of these campaigns, over 800 had raised money for theater projects.


### Analysis of Outcomes Based on Launch Date
In all months, successful campaigns are more common than failed ones. In fact, in all but three months of the year, August, October, and December, campaigns were 70% more likely to be successful than to fail (/kickstarter-analysis/outcomes_without_outliers.png). 


The best time to launch a theater fundraiser, however, is in the late spring or early summer. During these months, successful campaigns are significantly higher than failed ones. April and May campaigns are more than twice as likely to succeed than fail: [successes were 113% higher in April and 104% higher in May than failures] (pct_higher_by_month.png). 


The hardest months to launch occur towards the end of the year. In August successes outstripped failures by only 53%. In October that ratio fell to 30%. And in December successes were only 6% more likely than failing campaigns.


### Analysis of Outcomes Based on Goals
Because I had identified the top line of the Kickstarter data set using IQR, I determined that amounts above $35,000 were outliers, and were not solid bets for Louise to base her campaign goal upon. I focused on the range up to $35,000


I found that plays that raised up to $5,000 had significantly higher levels of success than failure. From the range of $5,000 to $15,000 successes were only slightly higher than failures, but the range from $5,000 up to $25,000 had differences of less than 10% [between the two factors] (outcomes_based_on_goal_catgories.png).


Above $25,000, failures outstrip successful campaigns by 20% or more. Above $35,000 the numbers were volatile, with advantage switching back and forth–but because I had already determined these to be outliers, I didn’t put much stock in this part of the graph anyway.


### Challenges and Difficulties Encountered
The challenge in the data came from the large number of outliers, which I feared might skew the tables I created and cause me to give Louise bad advice about launching her campaign.  When I ran a statistical analysis on the Kickstarter data, I found a mean goal of $71.938.86 with a  median goal of $5,000. This was my first indicator of significant outliers. It also turned out that the range soared from a maximum goal of $100,000,000 to a minimum goal of $1. Even with more than 4,000 data points, this was [cause for concern] (Statistcal_results_kickstarter.png).


To further complicate things, the standard deviation of the set of goals was $1,693,312.89, which was many times the average goal of $71,938. This indicated to me that there were outliers in the upper range of values.


I ran an IQR analysis to determine the top line of the data set. The first quartile went up to $2,000, and the 3rd quartile went up to 15,000. This gave me an IQR value of $1,3000. I multiplied this number by 1.5 and added it to the Quartile 3 value to identify a Top Line of $34,500. I resolved to eliminate the data above that line, which turned out to be just over 500 of the 4,115 cases in the data file.  I was ready to run a follow-up look at the outcomes of successful and failing campaigns, to ensure that my recommendations were correct.


I also checked the graph I had created to show success ratios by levels of goals. I realized that I would not need to run a new graph, but I would advise the client that results above $35,500 were outliers and not reliable (many of those upper-range results showed successful fundraising campaigns, which might have misled us to push for more without a reliable rationale. Here are the two charts I made: the first with outliers included, the second with outliers removed. 


Outcomes Based on Months WITH Outliers
(Outcomes_months.png)


Outcomes Based on Months WITHOUT Outliers
(outcomes_without_outliers.png)


## Results


- What are two conclusions you can draw about the Outcomes based on Launch Date?
1. April and May are the most opportune times to launch the campaign.
2. Any of the first 7 months of the year offer a 70% or greater chance of success over failure.


- What can you conclude about the Outcomes based on Goals?
1. Louise should consider a goal no higher than $25,000, and the highest chances of success top out at $5,000
2. Goals up to $15,000 have a higher rate of success than failure.
3. Goals between $5,000 and $25,000 have similar rates of success and failure.
4. Goals between $25,000 and $35,000 have low ratios of success when compared to failures.
5. I would recommend that goals above $35,000 be ignored because of the factor of outliers in the data. Successful outcomes seem to exeed failures between $35,000 and $45,000, but these are based on only a handful of examples. Setting goals above $35,000 goals along with a higher level of risk because of the lack of data.


- What are some limitations of this dataset?
1. Huge outliers that threaten to skew the data if precautions aren’t taken, i.e. limiting the analysis to data falling below the median + 1.5 * IQR threshhold.
2. Outcomes data is in string/text format, making it a little harder to calculate percentages of success & failure. For deeper analysis, we would need to ‘clean’ this data to make it numeric and operable.
3. Regarding the fundraising goal, the data set doesn’t take into account other factors of fundraising, such as the support of a single, major donor or the presence of a fundraising support team on the success or failure of a campaign.


- What are some other possible tables and/or graphs that we could create?
1. I created a 2nd “Outcomes with Goals in the Normal Range” table, which eliminated outliers from the calculations. It didn’t really change the results of the data much, but I’m glad that I compiled the data, just to make sure.
2. I compared the failed and successful campaigns using percentages in my Outcomes by Month sheet. I went so far as to create a bar chart showing how much higher the percentage of successful than failing campaigns would be. It basically showed the same information as the line chart, but Louise might find it more relatable, so I will include it in my report. After all, there is no such thing as too much information on which to make a [decision] (pct_higher_by_month.png).
