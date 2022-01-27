![shutterstock_1536519293](https://user-images.githubusercontent.com/81991136/151305822-d3de0178-1643-4b4c-9f16-21960443c959.jpg)
# Loan_Default_classification
## Overview
For most of us, the first thing we heard about smart money habits is savings accounts. When you want to keep your money safe, give it to the bank to hold for you and you’ll earn interest on it every month. Banks are happy to give you interest on your deposits, because they use your money to give out loans to others and take interest from them. So when you deposit money in a bank, you are funding the loans of potential borrowers. And the interest you get back is a small cut of what the bank gets from the interest on the loan. This works for all parties and everybody’s happy.

But over the last couple of decades, this deal has stopped working for depositors. Since the 2008 recession, interest rates have crashed. And over the past 2 years it’s gotten even worse. Add in the inflation and you see that putting money in a traditional banks savings account will actually cost you money.

![fredgraph](https://user-images.githubusercontent.com/81991136/151306089-67c89576-d724-4f4b-804c-237d5a2515b7.png)

## Business Objective
Enter “Peer to Peer Lending”. Introduced in 2005 in the UK, Peer-to-peer lending is a form of online lending that connects individual borrowers and lenders. One person will apply for a loan on any peer to peer platform and a few investors will combine to fund the loan. The process is usually much quicker for the borrower, than applying for a loan at the bank, and the lenders get to keep all the interest without the bank taking most of it. There is a lot of skepticism from traditional financial advisors on this form of lending for many different reasons, but it is becoming more mainstream. According to [verifiedmarketresearch.com](https://www.verifiedmarketresearch.com/product/peer-to-peer-p2p-lending-market/), the industry valuation is at about 85 million dollars and is expected to reach 578 million by 2028, with a “Compound Annual Growth Rate” of over 28 percent. Something that can offset the higher interest rates is that unlike your savings account, these investment are not insured, and if the borrower defaults on his payments, which does happen, you lose your money. That’s the risk/reward tradeoff.

Now what if you can create an algorithm to predict if a loan will default. Then you can reduce the rate of defaulted loans, and take full advantage of the high interest. This is what I tried to do.
## Data Understanding
The loans I worked with are all loans from the [Lending Club](https://www.lendingclub.com/) platform. Lending club was one of the pioneers for this form of lending, and was one of the most popular. Since a year ago they changed their business and no longer handles P2P lending.

I will be working with close to half a million loans from 2016 to 2018, that had over 150 features. I have already cleaned in the Cleaning and sampling notebook, and reduced the features down to 70. Check out that notebook for more details.

## Methodology

I had many features to use, and had to find a way to reduce the dimensionality. I started off with training my model on only the most obviously important features for a loan, like annual income or credit score. After that I tried using all the features witha PCA to reduce the dimensionality. After that I tried training on only a subset of the data that had much higher interest rates because of the higher risk, to try to get more value.

## Model Results

![image](https://user-images.githubusercontent.com/81991136/151380043-bf25b909-502d-4173-b4c0-013d23e219c3.png)

The best accuarcy I got was 90%, and 89% precision score, using all the features and a logistic regression.

When training on the high risk loans only, I got 85% accuracy and 80% precision, which considering the 37% default rate, is pretty impressive. And with the high interest rates, It's a good deal.

## Next Steps 

* Because lending club has changed their business and no longer is a P2P platform, I need to test this model on some other platforms loan applications.
* I need to get more current data, as the loans I was working with up to 2018.
## For More Information 

Review the detailed analysis in the Final Notebook or the presentation slides.

If you have any questions, reach out to me on [linkedin](https://www.linkedin.com/in/mendy-nemanow-2594ab225/)

## Repository structure
```
├── [Sample_datasets]
├── .gitingore
├── Cleaning_samling.ipynb
├── Main_notebook.ipynb
└── README.md
```
