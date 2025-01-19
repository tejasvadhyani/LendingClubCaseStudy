# LendingClubCaseStudy
> The LendingClubCaseStudy is a data analysis project aimed at understanding the factors that contribute to loan defaults. By analyzing historical data on past loan applicants, this project seeks to identify patterns and strong indicators of default. The insights derived will enable more informed decision-making for loan approvals.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- <b>Provide general information about your project here.</b><br/>
This project's aim is to assist bank in identifying high-risk applicants, optimizing loan offerings, and reducing overall portfolio risk.
- <b>What is the background of your project?</b><br/>
LendingClub is a lending platform where individuals and institutions can lend money to borrowers. Like any financial institution, LendingClub faces the challenge of minimizing loan defaults while maximizing profitability. Understanding the factors that drive loan defaults is crucial for maintaining a healthy lending portfolio and ensuring the long-term sustainability of the business.
- <b>What is the business probem that your project is trying to solve?</b><br/>
The primary business problem addressed in this study is the identification of patterns and variables that strongly indicate the likelihood of loan defaults.
- <b>What is the dataset that is being used?</b><br/>
We received a `loan.csv` dataset. It consist of `111` columns defining various attributes related to the loan applications that were accepted by the bank.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- From Univariate analysis on unordered categorical variable we concluded that every unordered categorical variable follows power distribution law. Although there are certain part of plot which looks outlawed but in general power distribution law is followed.
- From Univariate analysis on ordered categorical variable, we concluded insights as follow: 
    - Maximum loans taken are of 3 year term. 
    - Maximum loans taken interest rate lies between 9% - 15%.
    - Most of the A or B grade customers are granted loan. This indicate that bank want to take lowest possible risk of default in granting loans.
    -  It is observed that for few sub-grades, such as A4, B5 are granted more loans than A1 while A1 is considered as low risk grade. The reason for it could be that bank received less applications from A1 grade customers.
    - Bank is considering those customers more who has large employee length. 
    - With time loan applications are increasing. This could be due to various factors like economic conditions, bank policies, or changes in lending practices.
    - Most of the customers has credit history between 1990 to 2010.
- From Univariate analysis on unordered categorical variable, we concluded insights as follow:
    - Most loans request falls between $5000-15000. High loan requests are less common. High loan amounts indicate greater risk.
    - Funded amount follows a similar distribution as loan_amnt. This indicates efficient loan approval process as bank tends to fund amount close to loan amount requested.
    - Most of the EMIs lies between $200-500. High EMIs might correlate with large loans and can impact borrower ability to repay.
    - Most customers contains income less than 200000 but there are outliers in data.
    - Debt to Income ratio(DTI) value is less than 30 which indicates that bank grant loan to customers having low DTI as high DTI reflects high risk.
    - Most customer has 1-15 opened credit accounts. More no. of credits represents more risk associated with customer.
    - Almost all borrowers have zero public records, indicating good financial behavior. A small subset with 1 or more public records could be flagged as potentially higher risk.
- From Bivariate analysis, we concluded insights as follow (NOTE: Target/Dependent variable identified is Loan Status(loan_status)):
    - Customers who are taking 5 year term loan are defaulting most. Thus `term` can be considered as DRIVING VARIABLE.
    - As interest rates are increasing, chances of default are also increasing.Loans at high interest rate are vulnerable of default. Thus `int_rate` can be considered as a DRIVING VARIABLE.
    - Apart from very high funded loan amount, for other segment of funded loan amounts, charge off percentage is approximately same. Even for very high funded loan as well percentage difference could be just because of Randomness. Thus funded_amnt or loan_amnt or funded_amnt_inv cannot be considered driving variables.
    - Apart from very high installment amount, for other segment of installment, charge off percentage is approximately same. Even for very high installment as well percentage difference could be just because of Randomness. Thus installment cannot be considered driving variables.
    - As grade shifts from A to G, chances of default also increase. Loans to high grade customer are risky. Thus `grade` can be considered as a DRIVING VARIABLE.
    - From analysis on Home ownership field(`home_ownership`), we can see that customers who have OTHER ownership are getting charged off mostly. After that RENT, OWN, and in last MORTGAGE. MORTGAGE become further less risky if asset is mortgaged with bank. This column could be a DRIVING VARIABLE.
    - Less income customer loans are likely of charge off or default. As income is reducing charge off percentage is increasing. This could be the DRIVING VARIABLE.
    - Although verified customers look more risky but we cannot consider it as driving variable as there are chances that system has more number of verified customer than not verified. High no. of charged off verified customers shows that the Lending Club needs to revisit the verification process.
    - Small business loans have high tendency to get charged off, whereas Wedding loans have lowest tendency to get charged off. Thus `purpose` could be a DRIVING VARIABLE.
    - More `dti`(Debt to Income ratio), more is charge off percentage. Thus dti could be DRIVING VARIABLE
- Driving variables identified are term, int_rate, grade, home_ownership, annual_inc, purpose, dti.
- From Multivariate analysis, we concluded that there is a significant positive correlation between loan amount and installment; comparable correlation between loan amount and annual income, term and interest rate, debt to income ratio and Number of open accounts. Number of public records does not have a correlation between any of the parameters.


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Python - version 3.11.7
- Pandas - version 2.1.4
- numpy - version 1.26.4
- matplotlib - version 3.8.0
- seaborn - version 0.12.2
- Anaconda Navigator - version 2.5.2
- Visual Studio Code - version 1.96.4

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact
Created by [Yatin-Gupta] and [tejasvadhyani] - feel free to contact us!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
