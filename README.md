# -Risk-Averse-Loan-Data-Transformation-and-Analysis-for-Credit-Risk-Modeling


# Introduction to the Project
1.The loan data we were given is a sample from a larger dataset that belongs to a bank based on the US, therefore all the values given are in dollars $ we need to provide an equivalent in euros

2.every categorical variables must be quantified

3.We need to change text columns into numbers based on the information they contain

4.for others,(other than date values) we only care if they provide positive or negative connotations, so we'll turn them into dummy variables that holds either zero or one

5.furthurmore, when we're measuring creditworthiness we need to be extremely risk-averse and distrustful for any unavaliable data

6.missing information suggests foul play because loan applications are self reported

7.to elborate, since candidates fill out their applications manually so if the information isn't avaliable just assume the worst

8.the worst varies from one column to another so the team has provided us with casting directions for each variable in the dataset, therefore as we go through the dataset we'll usually know whether we should use the min,max or some other value when taking care of missing data

# Task & Responsabilities
## Examine the Dataset (Get familiar with a loan data .csv file):
The dataset contain both categorical and numerical values as well as headers defining each column
each row consists of information for the account of a loan candidate's application or account

ID:A unique LC assigned ID for the loan listing.

Issue_date:The month which the loan was funded

Loan_amount:The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.

Loan_Status:Current status of the loan

Funded_amount:The total amount committed to that loan at that point in time.

Term:The number of payments on the loan. Values are in months and can be either 36 or 60.

Interest_rate:Interest Rate on the loan

Installment:The monthly payment owed by the borrower if the loan originates.

Grade:LC assigned loan grade

Sub_grade:LC assigned loan subgrade

Verfication_Status:Indicates if the borrowers income was verified by LC, not verified, or if the income source was verified.

URL:URL for the LC page with listing data.

Address_State:The state provided by the borrower in the loan application
Total_Payment:Payments received to date for total amount funded.

# Cleaning & Preprocessing
Importing the Data
Import NumPy package
for easier viewing we'll call numpy set_printoptions function, we'll use this to improve the way we see outputs on the screen (Specifying these arguments won't alter the numerical values NumPy uses to compute mathematical opreations, it'll only affect how we see their values on the screen
Suppress = True, this'll stop NumPy from using scientific notations to express numbers
linewidth = 100, extend the number of characters we can fit into a single line of output to 100, 100 is often satsfies showcasing all the elements we need to see on the same line
precision = 2, only use the first two digits after the decimal points, more than enough to get a good idea of the numbers on the screen
Setting these print options will ensure we don't often see rows of an array displayed over multiple lines which will allow us to interpret the results more easily
store the loan data into a variable

# Checking for Incomplete Data
First try importing the data using (np.Loadtxt function) as it will return an error message if the dataset contain missing values & then displaying it after importing it, it'll return an error message indicating the dataset failed to convert strings to floats
switch to (np.genfromtxt()) the cell'll return values without an error
then we'll perform simple data cleaning technique

Splitting the Dataset

Splitting the Columns

Re-importing the Dataset

The Names of the Columns

Creating Checkpoints:

Manipulating String Columns

Issue Date

Loan Status

Term

Grade and Subgrade

Filling Sub Grade

Removing Grade

Converting Sub Grade

Verification Status

URL

State Address

Converting to Numbers

Checkpoint 1: Strings

Manipulating Numeric Columns

Substitute "Filler" Values

ID

Temporary Stats

Funded Amount

Loaned Amount, Interest Rate, Total Payment, Installment

Currency Change

The Exchange Rate

From USD to EUR

Expanding the header

Interest Rate

Checkpoint 2: Numeric

Creating the "Complete" Dataset

Sorting the New Dataset

Storing the New Dataset

Save it to an external .csv file to pass it to the other data scientists on the team
They'll contstruct a Credit Risk Model (CRM) that measures probability of default for every personal account

The data analyst goal is to obtain a clean & preprocessded dataset we'll note down all the changes we're making to the original dataset


