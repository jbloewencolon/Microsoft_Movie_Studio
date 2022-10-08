# Microsoft Movie Studio: A Romance to Make Millions

![hearts-dollars.jpg](attachment:hearts-dollars.jpg)

# Overview

## Business Understanding
With a host of other tech giants getting in on the movie business, Microsoft wants get in on the action by creating a new movie studio. Since they are new to the game and know so little about the industry they have hired us to explore and analyze which movies are making the most at the box office. After some data wrangling and processing, we have settled on three major insights and deliverables! Focusing on *return on investment, risk analysis of film budget tiers, and popular genres*, we suggest that Microsoft needs to 1) go big with its production budgets, 2) focus the majority of its budget on producing big "blockbuster" films, and 3) consider particular genres like drama and romance (at least according to this limited data set).

## Source and Description of Data 
We have settled on three main data repositories in order to make our case to Microsoft: Box Office Mojo (BOM), The Numbers (TN), and Rotten Tomatoes (RT). We chose both BOM and TN because of their broad inclusion of production budget and income numbers both domestically and worldwide. We ultimately focused primarily on budget and worldwide gross because the worldwide gross includes the domestic numbers as well. The RT data set was valuable for its inclusion of genres and ratings which allowed us to narrow down the types of films that seem to get the freshest (most valuable) reviews, in order to keep Microsoft as a "must-watch" studio.

## Data Understanding and Analysis
In preparing the data, we knew we wanted to merge both BOM and TN in order to get the broadest possible set of gross income values for the domestic and worldwide releases in addition to production budgets. To help Microsoft know which movies make the most, we needed to make sure we had data on what movies were actually making (and costing!). And because the worldwide gross includes the domestic gross, we filled any missing worldwide rows with the same data from its partnered domestic column.

With the RT data, we wanted to focus primarily on genre types and their critical review. While we would love to include the "box_office" numbers, there are just so few (340 out of 1559 entries) that any insights would be suspect.

### First Insight: The relationship between "Production Budget" and "Gross Income"

* Our first intuition was to see what the actual return on investment was for production budgets. 


* At first glance, it seems like there is a pretty strong correlation between the amount of money a studio spends on a film and the amount of return they get. We wanted to pin this correlation down, so we turned our scatter plot into a regression plot, and then used scipy stats to create a line regression that could give us insight to how much actual return a studio would get per dollar spent.

* As it turns out, it looks like the studios can expect to get about 3 dollars back for every 1 dollar they add to their production budget. Not bad!

### Second Insight: Not all film budgets are created equal!

* But everyone knows that there are different tiers of films. Ranging from indie to blockbusters. So how do we take into account the budget tier of a film? We went to [Film Lifestyle](https://filmlifestyle.com/film-budgets/) in order to get a sense about what seperates the budgets of film tiers and then created a function to help us parse out the different film types we think Microsoft should be aiming for. We dropped the lowest tier of films (student films and others) that had budgets of less than $10000.

* The above graph helps us see that while low budget films might offer the biggest return on investment, they also come with the highest deviation, which means they are VERY risky! But how risky?

### Blockbusters are the safest bet!

* As it turns out, blockbusters are actually the safest bet for making money, even if they might not offer the largest ROI. With the outliers removed, our graph does not quite indicate the level of risk/reward for low budget and moderate budget films, but it gets the larger point across.

## Third Insight: There Are Trends in Which Genres of Film are More Critically Rated

* We finally get to the Rotten Tomatoes dataset! The goal here is to figure out what TYPES of movies that Microsoft should make in order to maintain a positive standing among movie goers as a studio that produces "must-see" movie events that will then generate more revenue. 

* So first, we look to MPA rating, to see if there is any correlation between the rating its given and the how positive its reviews are. Turns out, PG-13 movies typically get the most positive ratings.

* According to our plot, the top 5 positively rated genres are drama, romance, musicals, family films, and comedies. The least positively rated movies are horror, science fiction, westerns, and action films. This strikes us as unlikely, but that could be a limitation of this dataset. 

# Conclusion

According to our three data insights above, it looks like if Microsoft wants to be successful in the movie industry they need to:
   1. Not be afriad to spend big on their production budgets
   2. Focus on producing primarily "blockbuster" type films while carefully taking risks with smaller budget films
   3. Produce films from genres that generate the highest positive critical reception: PG 13 and R rated films in the 
       categories of Drama, Romance, Musicals, Family, and Comedy.

# Summary

While we happily trust our analysis on the budget production, return on investment, and film tier, we are suspect of the conclusions involving genre. This is due to lack of data set. Given time constraints, we were not able to access a data set that connected genre, production budget, and gross income, which means we cannot actually draw any correlation between genre type, critical review, and ROI.

# Questions?
For a full analysis please check the Jupyter Notebook or slide presentation.

Further questions? Contact Jordan Loewen-Colón @ jbloewen@syr.edu
