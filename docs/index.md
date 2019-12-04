# Social graphs and interactions 2019 - A Stack Overflow Study

[I'm an inline-style link with title](https://nbviewer.jupyter.org/github/MadsVSChristensen/socialgraphs-project/blob/master/Project-assignment.ipynb 'Explainer notebook')

## Central idea

As a software engineer stackoverflow is used regularly, over not just a students lifetime at DTU, but also through the career. It is therefore entertaining to look into which questions or problems other people in the same situation deals with. The idea behind the project is to study stackoverflow's top questions over the last 10 years, to recognize the evoultion of programming languages and identify which problems relates to which languages. We also look into which words are important to a programming language. Furthermore we create a network of programming languages and detect communities within the network.

## Dataset

The dataset is pulled from the StackExchange API (https://api.stackexchange.com/). It consists of the top 100 questions every half month, based on score in descending order for the described timeframe. The API only allows for pulling 100 questions at a time, which is why we pull for every half month. This is done for the last 10 years, resulting in 2400 questions a year and a total of 240000 questions. The data is stored as a json object where the values from the tags, score, title and body keys is used for further processing. The dataset is around 30 mb in total.

## Analysis of network and text

The page should contain your network and text analysis (that's the main part).

### Network

#### Popular tags

First we wish to find the most popular subjects on Stack Overflow. We do this by taking each questions tags and grouping them together. Here we count the number of occurences and we find the following results:

![alt text](https://raw.githubusercontent.com/MadsVSChristensen/socialgraphs-project/master/docs/most-tags-all-time.PNG 'Tag total occurences')

There is a very clear top 4, and an even more clear winner; Javascript. Javascript appears approximately 1400 times in the 12000, meaning 12\% of all questions are about Javascript.
Interestingly android has twice the number of tags of ios, finally settling the debate about which is the most popular mobile operating system. However, this is more likely due to android being easier accessible to new programmers.

But how have these subjects popularity developed over time? We investigate the 6 most popular tags of all time, and see their development through the last 10 years.

![alt text](https://raw.githubusercontent.com/MadsVSChristensen/socialgraphs-project/master/docs/tags-pr-year-for-6-most-pop.PNG '6 most popular tags. Shown for each year')

As can be seen from the bar plot, most of the tags fluctuate quite a bit. Especially c++ which tripples its amount of occurences in 2019. C++ has seen a resurgance the last few years<sup>1</sup>, but unfortunately nothing explains a development this wild. This is likely due to a random outlier in our data, even if we have 3600 tags from 2019.

We also se python increase in popularity, this correlates well with the trend seen in larger datasets and analyses<sup>1</sup>.

#### Network of tags

Each question has one or more tags, where you can tag more subjects if your questions has correlation to more than one subject. We want to see which tags are well connected and which groups of tags may appear.

With Force Atlas 2 we visualize a network labeling the 25 tags with highest degree.

![alt text](https://raw.githubusercontent.com/MadsVSChristensen/socialgraphs-project/master/docs/fa2v1.PNG 'Logo Title Text 1')

Below with highlights:

![alt text](https://raw.githubusercontent.com/MadsVSChristensen/socialgraphs-project/master/docs/fa2v1-with-highlights.PNG 'Logo Title Text 1')

![alt text](https://raw.githubusercontent.com/MadsVSChristensen/socialgraphs-project/master/docs/degree-hist-zoomed.PNG 'Logo Title Text 1')

![alt text](https://raw.githubusercontent.com/MadsVSChristensen/socialgraphs-project/master/docs/react-tags-pr-year.PNG 'Logo Title Text 1')

## Download dataset

There should be download options for data sets (so the user can play around).

## Explainer notebook

You must link to the Explainer Notebook (more details below) that explains the details of your analysis (including all of the machine learning, the model selection, etc). You can achieve this with a link to an IPython notebook displaying on the nbviewer.

## References

1. https://www.tiobe.com/tiobe-index/