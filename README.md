
# Late Loan Identifier

This is a project used data from Paipaidai（拍拍贷）, a past peer-to-peer lending industry that provides private financial service to general public. 


## Authors

- [@Kayannn123](https://www.github.com/Kayannn123)
- [@PoliteVincent](https://github.com/PoliteVincent)

## Data Description

Collecting data from late 2015 to early 2017, the data aims to present the past loans-related behavior of borrowers.
## Analysis of User group
![LateLoanIdentifier\Histogram of Loan Amount.png](https://github.com/Kayannn123/LateLoanIdentifier/blob/main/Histogram%20of%20Loan%20Amount.png)

Paipaidai originated as a small loan platform, so this image aligns well with the scale of the platform. However, based on the understanding that small loans are the primary loan amount, we can infer that the users of PPDai are likely individuals who cannot obtain small loans through formal channels. Therefore, it is highly probable that these loans come with high interest rates.

![Loan Amount vs Loan Interest Rate.png](https://github.com/Kayannn123/LateLoanIdentifier/blob/main/Loan%20Amount%20vs%20Loan%20Interest%20Rate.png)
By attempting to combine ratings and interest rates, we can demonstrate that individuals willing to take out small loans are unable to do so through formal institutions such as banks. Hence, their ratings are likely to be relatively low. Additionally, although some individuals have high loan amounts, their interest rates remain low due to their ratings. However, individuals with a rating of B appear particularly risky, as their loan amounts and interest rates are widely distributed, indicating that there isn't a clear distinction in creditworthiness among people with this rating.

![Piecharts of Interest Rate and Rating.png](https://github.com/Kayannn123/LateLoanIdentifier/blob/main/Piecharts%20of%20Interest%20Rate%20and%20Rating.png)
From this graph, it's evident that ratings have a significant impact on interest rates. However, it also suggests that ratings are not entirely reliable. If all individuals rated as 'A' do not receive higher interest rates for higher loan amounts, as a small loan platform, PPDai needs to acknowledge the risk that some borrowers might attempt to manipulate their ratings to secure higher loan amounts at lower interest rates or even default.

![Frequency of Loan Types at Each Loan Amount.png](https://github.com/Kayannn123/LateLoanIdentifier/blob/main/Frequency%20of%20Loan%20Types%20at%20Each%20Loan%20Amount.png)
The prevalence of e-commerce loans in high loan amounts indicates that the rise of e-commerce live streaming in 2017 has to some extent fueled the trend of premature consumption. Many individuals may have been induced to take out loans by live streaming promotions.

![Bar Plot of Verification vs Overdue Status.png](https://github.com/Kayannn123/LateLoanIdentifier/blob/main/Bar%20Plot%20of%20Verification%20vs%20Overdue%20Status.png)
This graph essentially proves that the more authentication an individual undergoes, the lower their default rate tends to be. This could be attributed to the correlation between identity verification and credibility. Considering the aggressive debt collection practices of early lending platforms, authenticated users are inclined to reduce the likelihood of default.

![Bar Plot of Age vs Loan Amount.png](https://github.com/Kayannn123/LateLoanIdentifier/blob/main/Bar%20Plot%20of%20Age%20vs%20Loan%20Amount.png)
This graph not only demonstrates the trend of premature consumption among young people but also corresponds to later models. It is highly likely that the borrowing behavior of the older generation is influenced by young individuals attempting to evade potential debt collection by using their elders' identification.


## Building of Model
We first utilized a decision tree for feature selection, followed by establishing a logistic regression model, achieving an impressive accuracy of 90%.
## Reflection
As my first personal data analysis project, I must admit that I had many erroneous preassumptions before building the model. For instance, I habitually assumed that the initial rating would have a significant impact on defaults. However, it turned out that because the initial rating didn't accurately classify borrowers, it led to unexpected defaults. Additionally, some of the business aspects of the PPDai platform we selected for analysis no longer exist, resulting in data limitations. Consequently, we are unable to generalize this model to other datasets. I welcome any feedback and suggestions from everyone.
