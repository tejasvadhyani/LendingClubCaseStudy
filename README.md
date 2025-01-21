# LendingClubCaseStudy
> The LendingClubCaseStudy is a data analysis project aimed at understanding the factors that contribute to loan defaults. By analyzing historical data on past loan applicants, this project seeks to identify patterns and strong indicators of default. The insights derived will enable more informed decision-making for loan approvals.


## Table of Contents
* [General Info](#general-information)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)

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
- From Univariate analysis of unordered categorical variables we concluded that every unordered categorical variable follows power distribution law. However, there are certain part of plot which looks outlawed but in general power distribution law is followed.
- From Univariate analysis on ordered categorical variables, we concluded insights as follows: 
    - Maximum loans taken are of 3-year term. 
    - Maximum loans taken interest rate lies between 9% - 15%.
    - Most of the A or B-grade customers are granted loans. This indicates that bank want to take the lowest possible risk of default in granting loans.
    -  It is observed that for few sub-grades, such as A4, B5 are granted more loans than A1 while A1 is considered as low-risk grade. The reason for this could be that the bank received less applications from A1-grade customers.
    - Bank is considering those customers more who has large employee length. 
    - With time loan applications are increasing. This could be due to various factors like economic conditions, bank policies, or changes in lending practices.
    - Most of the customers have a credit history between 1990 to 2010.
- From Univariate analysis of quantitative variables, we concluded insights as follows:
    - Most loan requests fall between $5000-15000. High loan requests are less common. High loan amounts indicate greater risk.
    - Funded amount follows a similar distribution as loan_amnt. This indicates an efficient loan approval process as bank tends to fund amounts close to the loan amount requested.
    - Most of the EMIs lie between $200-500. High EMIs might correlate with large loans and can impact borrower's ability to repay.
    - Most customers have income less than 200000 but there are outliers in the data.
    - Debt to Income ratio(DTI) value is less than 30 which indicates that bank grant loan to customers having low DTI as high DTI reflects high risk.
    - Most customer has 1-15 opened credit accounts. More no. of credits represents more risk associated with customers.
    - Almost all borrowers have zero public records, indicating good financial behavior. A small subset with 1 or more public records could be flagged as potentially higher risk.
- From Bivariate analysis, we concluded insights as follows (NOTE: Target/Dependent variable identified is Loan Status(loan_status)):
    - Customers who are taking 5-year term loans are defaulting most. Thus `term` can be considered as DRIVING VARIABLE.
    - As interest rates are increasing, chances of default are also increasing. Loans at high interest rates are vulnerable to default. Thus `int_rate` can be considered as a DRIVING VARIABLE.
    - Apart from the very high funded loan amount, for other segments of funded loan amounts, charge-off percentage is approximately same. Even for very high funded loans as well percentage difference could be just because of Randomness. Thus funded_amnt or loan_amnt or funded_amnt_inv cannot be considered driving variables.
    - Apart from the very high installment amount, for other segments of installment, charge-off percentage is approximately same. Even for very high installments as the percentage difference could be just because of Randomness. Thus installment cannot be considered a driving variable.
    - As the grade shifts from A to G, chances of default also increase. Loans to high-grade customers are risky. Thus `grade` can be considered as a DRIVING VARIABLE.
    - From the analysis of the Homeownership field(`home_ownership`), we can see that customers who have OTHER ownership are getting charged off mostly. After that RENT, OWN, and lastly MORTGAGE. MORTGAGE becomes further less risky if the asset is mortgaged with a bank. This column could be a DRIVING VARIABLE.
    - Less-income customer loans are likely to charge off or default. As income is reduced, the charge-off percentage increases. This could be the DRIVING VARIABLE.
    - Although verified customers look more risky but we cannot consider it as a driving variable as there are chances that the system has more number of verified customer than not verified. The high no. of charged-off verified customers shows that the Lending Club needs to revisit the verification process.
    - Small business loans have a high tendency to get charged off, whereas Wedding loans have lowest tendency to get charged off. Thus `purpose` could be a DRIVING VARIABLE.
    - More `dti`(Debt to Income ratio), more is charge off percentage. Thus DTI could be DRIVING VARIABLE
- Driving variables identified are term, int_rate, grade, home_ownership, annual_inc, purpose, dti, addr_state.
- From Multivariate analysis, we concluded that there is a significant positive correlation between the loan amount and installment; the comparable correlation between the loan amount and annual income, term and interest rate, debt to income ratio, and Number of open accounts. The number of public records does not have a correlation between any of the parameters.


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Python - version 3.11.7
- Pandas - version 2.1.4
- Numpy - version 1.26.4
- matplotlib - version 3.8.0
- seaborn - version 0.13.2
- Anaconda Navigator - version 2.5.2
- Visual Studio Code - version 1.96.4

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Contact
Created by [Yatin-Gupta] and [tejasvadhyani] - feel free to contact us!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
