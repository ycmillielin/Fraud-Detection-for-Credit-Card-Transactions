# Fraud-Detection-for-Credit-Card-Transactions

### Description of data:
The dataset includes credit card transaction data from a US government organization in 2006. The purpose is to identify transaction fraud. The dataset contains 10 fields and has 96,753 records, with 1,059 records labeled as fraud. Two of the fields are numerical and the others are categorical.

![Screen Shot 2022-09-01 at 2 16 29 PM](https://user-images.githubusercontent.com/96958028/188014582-28efdb27-2e40-436b-a979-4ea745222b35.png)

### Data Cleaning:
  - Filterng: Only keep purchasing data whose transtype is ‘P’, and remove one single transaction amount which is over 3 million dollars.
  - Filling in Merchnum: Replace 0 with NaN; Mapped with corresponding Merch description
  - Filling in Merch state: Mapped with corresponding Merch zip, Merchnum and Merch description
  - Filling in Merch zip: Mapped with corresponding Merchnum and Merch description
