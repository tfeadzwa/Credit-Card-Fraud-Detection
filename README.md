# Credit card fraud detection for banking using machine learning

## A web application for analyzing bank transactions and detecting fraud.

Welcome to the Credit Card Fraud Detection project repository! This project leverages machine learning techniques to tackle the pervasive issue of fraudulent credit card transactions. By analyzing a dataset comprising both legitimate and fraudulent activities, our goal is to develop a robust fraud detection model that aids in proactive monitoring and prevention. Follow along to learn more about the problem statement, dataset, methodology, and insights gained from this endeavor. Let's work together to safeguard financial transactions and protect customers from fraudulent activities.

## Understanding and Defining Fraud

Credit card fraud is any dishonest act and behaviour to obtain information without the proper authorization from the account holder for financial gain. Among different ways of frauds, Skimming is the most common one, which is the way of duplicating of information located on the magnetic strip of the card. Apart from this, the other ways are:

- Manipulation/alteration of genuine cards
- Creation of counterfeit cards
- Stolen/lost credit cards
- Fraudulent telemarketing

## Business Problem Overview

For many banks, retaining high profitable customers is the number one business goal. Banking fraud, however, poses a significant threat to this goal for different banks. In terms of substantial financial losses, trust and credibility, this is a concerning issue to both banks and customers alike.

It has been estimated by [Nilson report](https://nilsonreport.com/upload/content_promo/The_Nilson_Report_Issue_1164.pdf) that by 2020 the banking frauds would account to $30 billion worldwide. With the rise in digital payment channels, the number of fraudulent transactions is also increasing with new and different ways.

In the banking industry, credit card fraud detection using machine learning is not just a trend but a necessity inorder to proactive monitoring and fraud prevention mechanisms in place. Machine learning helps banks to reduce time-consuming manual reviews, costly chargebacks and fees, and denials of legitimate transactions.

## Main process steps:

- dataset preparation(reading, cleaning etc),
- apply machine learning algorithms,
- visualization report with graphs, tables and transaction analysis
- comparison of the operation and accuracy of the three algorithms.

## Technologies used

1. Python v3+
2. Pandas, numpy, matplotlib, seaborn, sklearn
3. Streamlit

## Dataset

The problem statement chosen for this project is to predict fraudulent credit card transactions with the help of machine learning models.

In this project, customer-level data is analyzed which has been collected and analysed during a research collaboration of Worldline and the Machine Learning Group.

The project leverages an openly accessible dataset comprising credit card transactions, encompassing both genuine and fraudulent activities. This dataset serves as the foundation for training and assessing the efficacy of the fraud detection model. The dataset was obtained from [Kaggle Website](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud), a prominent online platform and community catering to professionals in data science, machine learning, and data research. The dataset has a total of 2,84,807 transactions, out of which 492 are fraudulent. Since the dataset is highly imbalanced, so it needs to be handled before model building.

## How to install and run

1. Clone project
   `git clone https://github.com/`
2. Open in code editor, for example VSCode
3. create a virtual environment via terminal:
   `pip install virtualenv `
   `virtualenv env`
   `source env\Scripts\activate`
4. Install dependencies via terminal.
   `pip install -U scikit-learn pandas numpy matplotlib seaborn`
5. Install streamlit in terminal
   `pip install streamlit`
6. Run project in terminal
   `streamlit run main.py`

## How to input "manual transactions" for verification

You have 3 csv files. The creditcard.csv file contains all transactions. In the other two files, transactions are divided into fraudulent and legal ones.

1. Open any csv file
2. Copy any line. For example: -1.1152878574425795,-19.1397328634111,9.28684735978866,-20.134992104854,7.81867331002574,-15.652207677206302,-1.66834770694329,-21.3404780994803,0.6418997011947,-8.55011032700099,-16.6496281595399,4.81815244707108,-9.44531478308794,1.3170562933234098,-7.24346097400378,0.830910291033798,-9.533257050393189,-18.750641147467398,-8.09264877340557,3.32675827497024,0.42720343146936,-2.1826919456095504,0.5205430723666421,-0.7605564151887328,0.6627666383972359,-0.948454306235033,0.12179592582979301,-3.3818429293561,-1.2565236213625801,0.20610286556509647,1
3. Delete ",1" or ",0" in the end.
4. Paste new line in input label and submit. For example: -1.1152878574425795,-19.1397328634111,9.28684735978866,-20.134992104854,7.81867331002574,-15.652207677206302,-1.66834770694329,-21.3404780994803,0.6418997011947,-8.55011032700099,-16.6496281595399,4.81815244707108,-9.44531478308794,1.3170562933234098,-7.24346097400378,0.830910291033798,-9.533257050393189,-18.750641147467398,-8.09264877340557,3.32675827497024,0.42720343146936,-2.1826919456095504,0.5205430723666421,-0.7605564151887328,0.6627666383972359,-0.948454306235033,0.12179592582979301,-3.3818429293561,-1.2565236213625801,0.20610286556509647 (At the end of the new line, I deleted ",1")

## Project Pipeline

The project pipeline can be briefly summarized in the following four steps:

- **Data Understanding:** This is the initial phase which involves loading the data and understanding the its features. This helps to choose the features that will be required for the final model.

- **Exploratory data analytics (EDA):** Performing Univariate and bivariate analyses of the data, followed by feature transformations, if necessary. For the current data set, because Gaussian variables are used, no Z-scaling is performed. However, skewness is checked in the data and mitigated if necessary, as it might cause problems during the model-building phase.

- **Train/Test Split:**After train/test split, which performed in order to check the performance of models with unseen data. Here, for validation, k-fold cross-validation method is used. An appropriate k value is choosen so that the minority class is correctly represented in the test folds.

- **Model-Building/Hyperparameter Tuning:** This is the final phase where different models are tested/applied and their hyperparameters are fine-tuned until the desired level of performance on the given dataset is reached.

- **Model Evaluation:** This phase involves evaluation of the models using appropriate evaluation metrics. Since the data is imbalanced it is is more important to identify which are fraudulent transactions accurately than the non-fraudulent, that is, employing an appropriate evaluation metric which reflects the project research goal.
