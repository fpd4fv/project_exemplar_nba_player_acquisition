# project_exemplar_nba_player_acquisition
Showcasing my project that uses a two stage approach combining unsupervised ML k-means clustering with supervised ML regression model to predict which high performing NBA players are underpaid. This repo will present my data-driven approach for recommending players for acquisition an NBA team.

Author: Francis Driscoll

Link to deliverable webpage: https://rpubs.com/fpd4fv/889757
This site will showcase my data-driven approach for recommending players for acquisition an NBA team.

Project Overview: This project was developed in response to a lab prompt in my foundations of machine learning course at the University of Virginia's School of Data Science
- Prompt: "You are a scout for the worst team in the NBA, probably the Wizards. Your 
general manager just heard about Data Science and thinks it can solve all the
teams problems! She wants you to figure out a way to find players that are 
high performing but maybe not highly paid that you can steal to get the team 
to the playoffs!"

Summary of Approach
I am using a two-stage approach that will combine an unsupervised machine learning clustering approach and a supervised machine learning regression model to make educated predictions about which high performing players are underpaid and thus ideal targets for acquisition.

1. Conduct unsupervised machine learning k-means clustering. This will take all relevant features into account and produce another feature, cluster, which will eventually aid in producing a more accurate supervised machine learning regression model. In order to decide the ideal number of clusters to use for this dataset, I will use a function to evaluate explained variance over a range of number of clusters in order to reveal which number of clusters maximizes explained variance while minimizing complexity

2. With clustering complete, I will turn to produce a 3d visualization that will show players that are performing highly amongst the stats most closely correlated with salary in order to reveal the high-performing players that are underpaid relative to their peers. In order to identify the features that are the most correlated with salary, I will develop a correlogram between all of the relevant features in the dataset.

3. I will then develop a supervised machine learning regression model to make predictions on what a player should be earning considering their performance stats. I will evaluate different regression models such as rpart2 decision tree regression and a generalized linear model to see which model produces the most accurate predictions. Equipped with salary predictions, I will investigate the players who had high performance metrics as seen from the 3d visualization and see if the models predicts that these players are underpaid.


How to access project
- Link to HTML file published online via Rpubs: https://rpubs.com/fpd4fv/889757 This webpage is the deliverable I designed to simulate a data science deliverable for a business setting. This webpage takes the viewer through my process for approaching this data and presents interactive visualizations, performance metrics from the models that I developed, analysis of the data, and final recommendations for the team.
- HTML file: ("fpd4fv_NBA_lab_twostage_knitr_tech.html") available for download. This is the html file that produces the webpage above. Downloading and opening this file will bring the user to the page via a browser window. 
- Rmd file: ("fpd4fv_NBA_lab_twostage_knitr_tech.Rmd") This Rmd file knits to produce the HTML file presented above. This Rmd file includes all of the code that cleans and prepares the data, runs the plots, runs and evaluates the models, etc. I have included lines to install packages "corrplot" and "plotly" that are necessary to produce the visualizations. These install packages lines are commented out in order to prevent interference with the knitting process. 
- Data: This project uses two datasets that are joined together after being imported. The player salary data ("10_kMeans_Clustering/nba_salaries_21.xlsx") is an xlsx file included in the repo. The library for importing data from an xlsx file (readxl) is included in the library code chunk. The player stats data ("nba2020-21-1.csv") is included in the repo.
