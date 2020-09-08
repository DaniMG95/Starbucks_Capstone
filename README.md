# Starbucks_Capstone

<img src="https://www.merca2.es/wp-content/uploads/2020/04/starbucks-coffee-e1585725335618.jpg">

This repository contains the analysis of starbucks data and the creation of a predictive model to predict which customer will or will not complete a starbucks product offer. 
The link to this story in my blog [here](https://medium.com/@dani16595/who-should-you-send-offers-to-42f8e33ae99e)  
This data will help us to answer 5 questions that we have about the offers in Starbucks and I also encourage to get interesting data to all who are watching this repository.  
In addition, an exhaustive process of data cleaning had to be carried out, together with class balancing, in order to finally be able to take out the predictive model.  
This model can help a Starbucks company a lot since it will be able to predict if a client is going to complete an offer and thus send offers only to clients who are going to complete them.


## Libraries
To start this repository contains the following libraries:
* **numpy** : The fundamental package for scientific computing with Python.
* **pandas** :  Fast, powerful, flexible and easy to use open source data analysis and manipulation tool, built on top of the _Python_ programming language.
*  **matplotlib.pyplot** : _Matplotlib_ is a comprehensive library for creating static, animated, and interactive visualizations in Python.
* **json** : Allows the reading and writing of json format files.
* **seaborn** : Data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
* **datetime** : date and time arithmetic is supported, the focus of the implementation is on efficient attribute extraction for output formatting and manipulation.
* **sklearn** : Simple and efficient tools for predictive data analysis


## Files
This repository contains the following files :
* **transcript.json** : File that contains the availability of each house along with cost depending on the date.
* **profile.json** : File containing all the details of each house, such as number of beds, bedrooms, average price, type of availability, description.
* **portfolio.json** : File containing all the reviews of each house.
* **Starbucks_Capstone_notebook.ipynb** : Notebook of jupyter, where is all the code that I have made with the due exits and all the comments of the obtained results.
* **requirements.txt** : It contains the requirements of all the libraries I have used.

## Motivation

Starbucks Corporation is an international coffee chain founded in Washington. It is the world's largest coffee company, with over 24,000 stores in 70 countries.  
In this repository we have been presented with a real-world problem, where the company Starbucks has provided us with the data of its customers as opposed to the use of its offers that are sent to it.  
For them Starbucks wants us to create a model that allows them to improve the sending of these offers and at the same time analyse their data to see if any valuable information is taken out.

### Instructions:

pip install -r requirements.txt

### Structure of the project

```bash
|   .gitignore
│   README.md
│   requirements.txt
│   Starbucks_Capstone_notebook.ipynb
│
├───data
        portfolio.json
        profile.json
        transcript.json

```

## Summary of results


With this data we have found many curiosities from customers, who should focus Starbucks to improve their sales, for example that do not attract young customers, between 18 and 22 years, which means that they are losing potential customers. One solution would be to create offers for customers between these ages.  
Another curious fact is that people who have a high income are not attracted to make purchases of their products, so some measures should be studied to improve the purchase ratio of these customers.  
And finally, it is analysed that customers are more attracted to the non-use of the offers than to their use, since most of the transactions that have been observed are related to purchases without the use of any offer received.  
Then in this project we had to perform some pre-processing actions of the data, to clean the noise they had and also to adapt the data to be processed by our predictive models, such as performing One shot encode, zero value elimination, normalization.  
In addition, I found that the data was not balanced and I had to balance this class by eliminating data from the majority class and replicating data from the minority class in order to have 50% of each class and avoid the problem of over-adjustment of the majority class.  
Finally, several predictive models have been generated, and a comparison has been made between them, and the one that has given us the best result is the SVM which predicts us with a 0.40 of F1 score and a 0.805 of AUC.