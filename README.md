# Ford GoBike System Data Exploration
##  By Yasmin Madjitey


## Introduction

> In this data exploration project, I decided to go with the Ford GoBike System because I find the bike-sharing system in general, interesting. It is an opportunity to look at the state of the system in general using the provided dataset as an example. I looked at what could influence the bike-sharing system. Could it be distance, time, or user type? As in when are most trips taken in terms of time of day or day of the week? How long does the average trip take? Does the above depend on if a user is a subscriber or customer?

> Or maybe, the age group? the older the person, the willingness to engage in bike-sharing. or gender? men are more willing to subscribe than women?

> Using univariate, bivariate and multivariate exploration, I looked at the cases mentioned above in detail using visualizations.

## Dataset

> The dataset consists of 183,412 entries in the dataset with 16 original columns/attributes in relation to individual rides made in the bike-sharing system. However, for better understanding, I extracted the days in which the service was started and ended into new columns. Some of the features include the duration of the ride, user type, members birth year, etc. The dataset covers entries for the month of February.
> Due some quality issues and inconsistencies in the dataset, the dataset was cleaned for analysis. The appropriate data types were assigned, inconsistent values were handled and new columns such as a distance column, calculated based on the provided latitude and longitude, was added to the dataset. The final dataset consists of more object variables than numeric ones.

#### Univariate Exploration
> A univariate exploration was carried out to look at how individual variables are distributed. I expect that user type, duration, distance, and start time will support my investigation. So I went ahead to look at each variable on its own. Given that the variables under scrutiny are of ordered category, ie. user type, and the extracted days of the week, I ordered them accordingly and then used sb.countplot() function to visualize the distribution.

> The distribution showed that trips occured within a 24 hour time frame. The start and end day plots looked the same and unimodal, depicting that the most trips ocurred on Thursday. The time of the day plot or hour plot is almost bimodal, with most trips starting at 8:00 and 17:00. This is not so surprising as 8:00 - 17:00 fall within the time most jobs start and end. Plotted on a cube root scale, the distribution of distance takes on a unimodal shape at about 13km. There are also more subscribers than customers in the dataset.

> Other features discovered during the univariate exploration include:
There are more male than female in the dataset and most of the members are 1988 borns.


#### Bivariate Exploration
> In this section, I investigated the relationships between pairs of the above mentioned variables in the data. Visualizing the relationship between the user type and distance covered, one can see that as members move from customers to subscribers, the distance covered increases, although there are much fewer subscribers along the lines of long trips. The bulk of customers and subscribers can be seen between trips of 8km and 20 km long.

> One would expect the distance covered by a trip to be in tune with the duration. The bulk of the data sat around 0-10 hours and 0-20 km. It can also be seen that, an increase in the trip duration does not neccessarily corespond with an increase in distance covered. This could be as a result of stops or pauses taken by the individual.

#### Multivariate Exploration
> In a plot looking at the relationship between user types, distance covered and duration, points for customers tend be smaller than for subscribers.Plotting this relationship on each level of user type, ie. customer and subscriber, there doesn't seem to a difference in their relationship between distance and duration. Which is to say that, distance covered or the trip's duration doesn't really depend on the type of user, be it a customer or a subscriber.


## Summary of Findings

>  To summarize my findings, I would like to hint at the fact that most trips started at 8:00 and 17:00 which is not so surprising as 8:00 - 17:00 fall within the time most jobs start and end. However, Thursday was the day of the week most trips are taken. Surprisingly, duration and distance covered does not depend on the user type eventhough there are more subscribers than customers in the dataset. Other external factors like promotional activities by the company will explain why there are more subscribers than customers.

> I also saw that more male than female use the service and people within the age group of 34 use the service most. This may help the company decide on where to focus its advertisements.

> Should there be data on the traffic system of the area under study, it could also help in understanding what influences people to engage in the bike-sharing system.


## Key Insights for Presentation

> 1. When are most trips taken in terms of time of day and day of the week? 
> 2. How long does a trip take? 
> 3. Does the duration of a trip depend on if a user is a subscriber or customer?
> The questions raised above look like something everyone would like to know hence, these would be in the presensation.

> For the presentation, I would focus on the duration of a trip, the distance covered, user type and time of the day and day of the week.
I would introduce the distribution of time of the day and day of the week under univariate exploration to answer the question, When are most trips taken in terms of time of day and day of the week? I used a countplot here since they are categorical variables.

> I would then answer the question, How long does a trip take? under bivariate exploration. I used a scatter plot here for numeric values.
Finally, a multivariate exploration was used to visualize the final question, Does the duration of a trip depend on if a user is a subscriber or customer?