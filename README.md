# Project Title

The title of this repo is Loan Qualifier APP. The Loan Qualifer collects an applicants credit score, Requested Loan amouint, Debit to Equity, and Home Value. After Collecting this data the app compares the data to a list of lenders and the lenders requirements for to lend. If the applicant meets the requirements the app will provide a list of lenders willing to lend to the applicant. If the applicant does not meet the requirements the app will tell the applicant no loans availble at this time.

---

## Technologies

The code is written in Python 3.7.
We imported the following:
csv
sys
fire
questionary

---

## Installation Guide

import csv
import sys
import fire
import questionary
from pathlib import Pat

from qualifier.filters.max_loan_size import filter_max_loan_size
from qualifier.filters.credit_score import filter_credit_score
from qualifier.filters.debt_to_income import filter_debt_to_income
from qualifier.filters.loan_to_value import filter_loan_to_value

# Calculate the monthly debt ratio
    monthly_debt_ratio = calculate_monthly_debt_ratio(debt, income)
    print(f"The monthly debt to income ratio is {monthly_debt_ratio:.02f}")

    # Calculate loan to value ratio
    loan_to_value_ratio = calculate_loan_to_value_ratio(loan, home_value)
    print(f"The loan to value ratio is {loan_to_value_ratio:.02f}.")

    # Run qualification filters
    bank_data_filtered = filter_max_loan_size(loan, bank_data)
    bank_data_filtered = filter_credit_score(credit_score, bank_data_filtered)
    bank_data_filtered = filter_debt_to_income(monthly_debt_ratio, bank_data_filtered)
    bank_data_filtered = filter_loan_to_value(loan_to_value_ratio, bank_data_filtered

---

## Usage
The loan qualifier will ask 5 questions, provide debt to income ratio and loan to value ratio if applicant does not qualify for any loans the screen will read like example 1 below. If the applicant qualifies for a loan the program will provide the monthly debt to income ratio and loan to value amount. If the applicant qualifies for a loan the program will also tell the applicant how many lenders are available and ask if the applicant wants to save the names of the lenders. If the applicant is qualifies then the screen will read like Example 2. 

Example 1 
<function load_bank_data at 0x000002125325FF78>
? Enter a file path to a rate-sheet (.csv): C:\Users\todid\Downloads\Starter_Code (6)\Starter_Code\loan_qualifier_app\data\daily_rate_sheet.csv
? What's your credit score? 800
? What's your current amount of monthly debt? 1000
? What's your total monthly income? 10000
? What's your desired loan amount? 59900
? What's your home value? 1000
The monthly debt to income ratio is 0.10
The loan to value ratio is 59.90.
Found 0 qualifying loans
No loans avaliable at this time
PS C:\Users\todid\Downloads\Starter_Code (6)\Starter_Code\loan_qualifier_app> 

Example 2 

? Enter a file path to a rate-sheet (.csv): C:\Users\todid\Downloads\Starter_Code (6)\Starter_Code\loan_qualifier_app\data\daily_rate_sheet.csv
? What's your credit score? 800
? What's your current amount of monthly debt? 1000
? What's your total monthly income? 10000
? What's your desired loan amount? 599000
? What's your home value? 1200000
The monthly debt to income ratio is 0.10
The loan to value ratio is 0.50.
Found 1 qualifying loans
?  Would you like to save the loans you qualify for Yes
[[['FHA Fredie Mac - Premier Option', '600000', '0.9', '0.43', '790', '3.6']]]



---

## Contributors

In addtion to me the GW Bootcamp TA, LA, and tutors help me create this project 

---

## License

The Source code is for educational purposes only and should not be used to qualify any applicant for a loan.  Feel free to use for any educational needs
