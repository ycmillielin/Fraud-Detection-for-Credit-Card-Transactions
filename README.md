# Fraud-Detection-for-Credit-Card-Transactions

### Description of data:
The dataset includes credit card transaction data from a US government organization in 2006. The purpose is to identify transaction fraud. The dataset contains 10 fields and has 96,753 records, with 1,059 records labeled as fraud. Two of the fields are numerical and the others are categorical.

![Screen Shot 2022-09-01 at 2 16 29 PM](https://user-images.githubusercontent.com/96958028/188014582-28efdb27-2e40-436b-a979-4ea745222b35.png)

### Data Cleaning:
  - **Filterng**: Only keep purchasing data whose transtype is ‘P’, and remove one single transaction amount which is over 3 million dollars.
  - **Filling in Merchnum**: Replace 0 with NaN; Mapped with corresponding Merch description
  - **Filling in Merch state**: Mapped with corresponding Merch zip, Merchnum and Merch description
  - **Filling in Merch zip**: Mapped with corresponding Merchnum and Merch description

### Feature Creation:
  - **New entities**: Link Cardnum and Merchnum with Merch state, Merch zip and Amount
  - **Day-since variables**: Measure how much time has passed since a certain transaction last appeared in the dataset
  - **Frequency variables**: Measure how often does a certain transaction appear over the past 0, 1, 3, 7, 14 and 30 days
  - **Amount variables**: The Average, Maximum, Median, Total, Actual/maximum, Actual/median, and Actual/total amount for a certain transaction over the past 0, 1, 3, 7, 14, and 30 days. 
  - **Relative velocity variables**: Measure the ratio of frequency of a transaction or amount spent in a small time window with a larger time window
  - **Day of week and state risk table**: Measurement of the probability of finding fraud on a certain day of a week or a certain state
  - **Benford’s law variables**: Measure whether the variables violate Benford's law
  - 522 new variables created in total

### Feature Selection: Apply Filter(Kolmogorov-Smirnov (KS)), Wrapper(Forward selection, Backward selection, SelectKBest) and Embedded methods(Lasso and Ridge regression), try 6 different assemblies for these methods to get 6 different sets of features to put into our models and see which subsets will have better performance

![Screen Shot 2022-09-01 at 2 40 38 PM](https://user-images.githubusercontent.com/96958028/188017946-e3aba2ad-0beb-4389-9f32-b06013d86922.png)

  
