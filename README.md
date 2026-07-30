# Telco Customer Churn Analysis

This is my first data analyst portfolio project. I wanted to work with a real business problem instead of a toy dataset, so I picked customer churn. It's something almost every subscription based company deals with, and it forces you to think like an analyst instead of just running code.

## The Problem
A telecom company is losing customers and losing a customer costs more than keeping one. I wanted to figure out which customers are most likely to leave and why. If I can answer that, the business can actually act on it instead of guessing.

## The Data
I used the [Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) from Kaggle. It has 7,043 customers, with details like contract type, how long they've been a customer, what services they have, how they pay and whether they churned.

## What I Did
I started by cleaning the data. There was a tricky issue where Total Charges was stored as text because of 11 blank values. It turned out those were all brand new customers with 0 months of tenure, so I filled them with 0 instead of guessing with an average.

After that, I created a couple of new columns to make the analysis easier: I grouped tenure into buckets and counted how many extra services each customer has. Then I explored the data to test a few hypotheses about what drives churn, made charts to actually see the patterns instead of just reading numbers and wrote up what I found along with what I'd recommend the business do about it.

## Tools
Python, using pandas, numpy, matplotlib and seaborn, all in a Jupyter Notebook.

## What I Found

1. About 26.5% of customers churned, which comes out to roughly $139,000 a month in lost revenue or over $1.6 million a year.

2. Contract type matters more than anything else. Month to month customers churn at 42.7%, while two year contract customers barely churn at all, at 2.8%. That's a massive gap.

3. New customers are the most likely to leave. Almost half of customers in their first year churn, and that rate drops steadily the longer someone stays.

4. These two things stack on top of each other. New customers on month to month plans churn over 51% of the time, making them the riskiest group in the whole dataset.

5. More add on services generally means customers stick around longer, though I had to dig into a strange result before that pattern became clear (it only holds true for customers who actually have internet service).

6. Electronic check users churn three times more than people who pay automatically.

## What I'd Recommend
Push month to month customers toward longer contracts, especially early in their time as a customer. Build some kind of outreach or check in process for customers in their first 90 days, since that's when churn risk is highest. Bundle services together so customers have more reason to stay. And look into why electronic check users are churning so much, then encourage them to switch to automatic payments.

## Files in This Repo
`churn_analysis.ipynb` has the full notebook with code and explanations. `Telco_customer_churn.csv` is the dataset. The `images` folder has the charts saved separately.

## About Me
Gursimar Kour. This is one of the first projects in my data analyst portfolio.
