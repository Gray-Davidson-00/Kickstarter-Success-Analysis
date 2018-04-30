# Project Luther
## Gray Davidson
## April 27th 2018

### Summary:

The files in this directory represent the source code, resulting datasets, analysis, presentation and writeup for "Project Luther," my second project in school at Metis data science bootcamp.  

The assignment was to scrape the web to gather a dataset and apply linear regression to that data.  In my case I chose to scrape kickstarter.com to learn about the effects of measurable decisions (total goal in $ for instance) on the likelihood of a successful outcome.  

I scraped 2400 active kickstarter campaigns, compiled the data into a usable dataset and ran three various regression models.  The conclusion was that while these metrics are lightly predictive of a good outcome, that prediction is mostly driven by the edge cases (total text is predictive, for instance, but mostly because having no text at all is predictive of failure).  

The entire project is written up on Medium here: https://medium.com/@gray.davidson.00/mapping-kickstarters-success-formula-ce985ed40919

### How to use these files: 

This directory contains a series of code files and several datasets.  To replicate this work: 

1. get_kickstarter_links.ipynb is run to scrape 2400 current kickstarter campaigns.  
2. The dataset 2400_links.txt contains the list of 2400 links extracted from kickstarter.com's 'explore' page on 4/25/18
3. all_scrapes.csv contains the total html text of the subsequently scraped pages saved as a python dictionary. (((Actually I could not include this file as it is 100+ MB)))
4. kickstarter_data_pickle.pkl contains the cleaned dataframe which resulted from pulling the relevant numerical data from these html pages.  This file is used in the three analyses.  
5. kickstarter__regression_model.ipynb contains ordinary least squares regression applied to the data in kickstarter_data_pickle.pkl.
6. kickstarter_lasso.ipynb contains OLS regression modified by the L1 Norm (Lasso) applied to the data in kickstarter_data_pickle.pkl.
7. kickstarter_grad_boosted_trees.ipynb contains a gradient boosted tree model applied to the data in kickstarter_data_pickle.pkl.
8. The scraping, data and analyses are visualized and presented in Luther_Proposal_Davidson.pdf