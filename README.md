# Chicago Voter Turnout

Over the last 10 presidential elections, voter turnout has failed to exceeded 58%. This nationwide trend extends to Chicago as well, where for this project I looked at voter turnout across the last four elections.

#### What explains this low voter turnout? 

I gathered data from a variety of sources to answer this question. I gathered demographic variables like income and age from the U.S. Census Bureau, local crime statistics from the City of Chicago’s Data Portal, street-level walkability scores from walkscore.com, and polling station locations from the Chicago Board of Elections.

All together, this gave me 28 features for my linear regression model.

#### Model Results

Almost all of my features were statistically significant, with my model producing a very decent R-squared of 0.864. The R-squared metric gives you a measure of how much of the variance in the data is explained by your model, so this result is telling me that over 85% of voter turnout variance can be explained by the model I produced. 

For this project, I wanted to focus mainly on the descriptive power of linear regression, so I didn’t include predictive optimization techniques like regularization or feature interaction, but if we wanted to do predictions into the future then these would be techniques worth exploring.

The percent of a precinct population which is disabled was statistically insignificant. This is especially surprising, given that being disabled is [one of the most commonly cited reasons](https://www.bloomberg.com/politics/graphics/2016-non-voters/) by non-voters for failing to vote come election time.

#### Significant Features

Among my 25 statistically significant features, some were obviously more impactful than others.

There are two features specifically that had massive effects on voter turnout: 
1. the percent of the population living below the poverty line
2. the percent of the population which speaks English

For example, two of the most impoverished regions of Chicago, Garfield Park and North Lawndale, together averaged just over 50% voter turnout during the past four elections, compared with 58% for Chicago as a whole.  And their poverty rate is over twice as high as the Chicago average.

Zooming out to all of Chicago, we continue to observe this inverse relationship between poverty and voting. My model indicates that holding everything else constant like age, education, and crime, for every 1% increase in the precinct population living below the poverty line, there is an associated 16% decrease in voter turnout. This relationship should be especially concerning, given that those community members living in poverty are among our most vulnerable citizens. 

Similarly, the data indicate that regardless of income, age, or crime, a 1% increase in the English speaking population is associated with a 32% increase in voter turnout. This result is also concerning, because immigrant and non-native English speaking communities typically have a harder time accessing local resources. Even more so than their poverty-stricken counterparts, members of this group are failing to make their voices heard come election time. 

#### Conclusion

The data provide a clear connection between voter turnout and demographic and precinct-level variables, with some variables being more impactful than others. 

Now that we have strong empirical evidence for the powerful connection between poverty, language, and voter turnout, we can turn to the question of how to address these issues and increase voter turnout in vulnerable communities.

For example, to help low-income voters cast their ballots we could focus on increasing awareness and access to early voting mechanisms like in-person early voting or Chicago’s Vote by Mail option. To address language-barriers the city could produce election material in different languages, and possibly consider staffing polling stations with bilingual staffers come election day. 

If anyone is interested in exploring my data set further, I put together a little dashboard available [here](https://github.com/alex-douglas/chi-voter-dashboard) which allows one to compare the relationship between different features in my feature-set, as well as get a better feel for the data more generally.
# chi-voter-turnout
