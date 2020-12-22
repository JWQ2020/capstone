# Starbucks Capstone Challenge

## Background and project overview
Many of Starbucks’ customers use the Starbucks rewards mobile app on their smartphones. Once every few days, Starbucks sends out a customer offer to users of the app, and also via other channels such as email and social media. Sending offers incurs a cost to Starbucks, not only the adminstrative costs of delivering the offer, but also the discount or the free item given to the customer. For this reason, Starbucks would like to know how popular these offers are. In other words, if Starbucks send out an offer, with the aim of encouraging the customer to make a certain purchase, how likely is the customer to take it up as a result, and to make the purchase? Knowing this, Starbucks can restrict the sending of offers to only those customers that are very likely to be responsive, rather than sending to everyone.

The project aims to use the data set provided by Starbucks to predict which of Starbucks’ range of offers a given customer is likely to complete.

Full background, a description of the analyses performed as part of the project, and a discussion of the results, can be found in the blog post 
https://myds.design.blog/2020/12/22/how-popular-are-starbucks-customer-offers/

## Key components
The key components of this project are 
1. The Jupyter notebook `Starbucks_Capstone_notebook.ipynb` containing the code that processes the Starbucks data set, and that runs the analyses to predict which offers customers are likely to complete.
2. The Starbucks data set, which is the basis of the investigation. These are held in the folder `data`. The data set comprises three json files: 
 - `portfolio.json` contains data on the portfolio of offers sent by Starbucks
 - `profile.json` contains demographic data for each of the customers in the data set
 - `transcript.json` contains a history of events, e.g. offers received, and transctions, related to each customer. Note that due to upload size limitations, the file has been uploaded as a .zip file, and should be unzipped before use. See instructions below.

## Other files
Processing of the Starbucks takes some time. Instead, you can simply load the already-processed data, which is contained in the following files:
1. `user_offer_mx`, which contains the offers received, viewed and completed by each customer
2. `user_offer_rates_mx`, which shows the offer completion rates performed by each customer
3. `user_trans_mx`, which shows the number of value of transactions performed by each customer.

## System requirements
The project was developed in Python 3.6.3, and requires Pandas version 0.23.3 or later.

## Instructions
1. The Starbucks data set folder, `data`, containing three files, should be downloaded to the same directory as `Starbucks_Capstone_notebook.ipynb`. The `transcript.zip` folder must be unzipped into `data`.

2. If, as recommended, the preprocessed files, `user_offer_mx`, `user_offer_rates_mx`, and `user_trans_mx` are used, you should ensure that these files are in the same directory as `Starbucks_Capstone_notebook.ipynb`. In the notebook, in the section immediately proceeding "1 Preprocessing", there is the following script:

```
# if you want to use the previously processed and cleaned data, then "YES", otherwise "NO"
load_user_offer_matrix = "YES"
```

You should ensure that the variable `load_user_offer_matrix` is assigned the value "YES" as seen above, before running the code in the notebook.

3. If you wish to perform the preprocessing yourself, then the files `user_offer_mx`, `user_offer_rates_mx`, and `user_trans_mx` are not required. You should ensure that load_user_offer_matrix is assigned the value "NO", before running the code in the notebook. 


## Acknowledgements
Acknowledgement is given to Udacity for the idea for the Capstone project and for the starter codes, and to Starbucks for providing the data set used in this project.
