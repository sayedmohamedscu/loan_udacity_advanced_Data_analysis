# Loan Dataset Exploration
## by ElSayed mohamed


## Dataset

In this investigation, we will explore the characteristics of loans that could be used to predict their APR. The main focus was on the original loan amount as it one of the main features, borrower's Prosper rating, loan term, borrower's stated monthly income
The dataset consists of borrower APRs and attributes of about 114K loans. The attributes includs original loan amount, borrower's Prosper rating, loan term, borrower's stated monthly income, as well as many other features such as borrower's employment status, debt to income ratio, current loan status etc. some data points were removed from the analysis due to very large stated monthly income I've considered them as outliers and missing borrower APR information.
The dataset can be found [here](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv), 
with feature documentation available [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0)



## Summary of Findings

after dealing with outliers and doing the data cleaning process, I've worked on the following

Distribution of Borrower APR

it is multimodal. there is a peak (small one )at 0.1 , large at the center of the distribution , small peak about 0.3 , large at 0.36 A small peak centered at 0.38
there are Only very few loans have APR greater than 0.43.

Original Loan Amount

the most common values are at 10K ,15K,20k ,25K

people like to have a number multiples of 5K :XD

Borrower APR vs. Prosper Rating

Interestingly, the APR decrease with the increase of borrow term for people with HR-C raings. But for people with B-AA ratings, the APR increase with the increase of borrow term. which make sense

Prosper Rating Effect on Relationship between APR and Loan Amount

The loan amount possitively increases with better rating. The APR decreases with better rating.

so, the relationship between APR and loan amount turns from negative to slightly positive when the * Prosper_ratings * are increased from HR to A or better.

BorrowerState: 12.7% of the loans belong to (clients) borrowers from (CA) California.

it's a defence mechanism,as people with A or AA ratings borrow more money, increasing APR could prevent them borrow even more and maximize the profit. on the other hand people with lower ratings tend to borrow less money, decreasing APR could encourage them to borrow more.

Borrower APR by Rating and Term

Interestingly, the APR decrease with the increase of borrow term for people with HR-C raings. But for people with B-AA ratings, the APR increase with the increase of borrow term. which make sense

the rating and term_effects on stated_monthly_income and loan_original_amount variables

## Key Insights for Presentation

I just focus on features that may affect the APR, which are features like original loan amount, Prosper rating. I started by showing the distribution of borrower APR and loan amount variable. Then, I showed with graphs (pandas or seaborn) the relationship between borrower APR vs loan_amount feature, also APR vs. rating. on the otherhand ,the effect of rating on ralationship between borrower APR feature and loan_amount feature, and the effect of the rating(categorical to num ) on relationship between borrower APR vs the terms.

### References

> https://www.investopedia.com/terms/r/revolving-account.asp 

>https://www.investopedia.com/terms/t/trade-line.asp

> https://en.wikipedia.org/wiki/Pearson_correlation_coefficient

