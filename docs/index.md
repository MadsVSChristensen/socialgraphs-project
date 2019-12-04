# Social graphs and interactions 2019 - A Stack Overflow Study
[I'm an inline-style link with title](https://nbviewer.jupyter.org/github/MadsVSChristensen/socialgraphs-project/blob/master/Project-assignment.ipynb "Explainer notebook")

## Central idea
As a software engineer stackoverflow is used regularly, over not just a students lifetime at DTU, but also through the career. It is therefore entertaining to look into which questions or problems other people in the same situation deals with. The idea behind the project is to study stackoverflow's top questions over the last 10 years, to recognize the evoultion of programming languages and identify which problems relates to which languages. We also look into which words are important to a programming language. Furthermore we create a network of programming languages and detect communities within the network.

## Dataset
The dataset is pulled from the StackExchange API (https://api.stackexchange.com/). It consists of the top 100 questions every half month, based on score in descending order for the described timeframe. The API only allows for pulling 100 questions at a time, which is why we pull for every half month. This is done for the last 10 years, resulting in 2400 questions a year and a total of 240000 questions. The data is stored as a json object where the values from the tags, score, title and body keys is used for further processing. The dataset is around 30 mb in total.

## Analysis of network and text
The page should contain your network and text analysis (that's the main part).

### Network

![alt text](https://github.com/MadsVSChristensen/socialgraphs-project/blob/master/docs/degree-hist-zoomed.PNG "Logo Title Text 1")
![alt text](https://github.com/MadsVSChristensen/socialgraphs-project/blob/master/docs/most-tags-all-time.PNG "Logo Title Text 1")
![alt text](https://github.com/MadsVSChristensen/socialgraphs-project/blob/master/docs/fa2v1.PNG "Logo Title Text 1")
![alt text](https://github.com/MadsVSChristensen/socialgraphs-project/blob/master/docs/react-tags-pr-year.PNG "Logo Title Text 1")
![alt text](https://github.com/MadsVSChristensen/socialgraphs-project/blob/master/docs/tags-pr-year-for-6-most-pop.PNG "Logo Title Text 1")

## Download dataset
There should be download options for data sets (so the user can play around).

## Explainer notebook
You must link to the Explainer Notebook (more details below) that explains the details of your analysis (including all of the machine learning, the model selection, etc). You can achieve this with a link to an IPython notebook displaying on the nbviewer.

