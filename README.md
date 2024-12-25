# lending_club_case_study

### ManishGautam.ipynb - this file contains all the code for the analysis, it's a Jupyter Notebook
### Lending Club Case Study.pdf - this file contains all the analysis and charts

100.0%
## Steps performed for the analysis
### 1. Importing main libraries
### 2. Loading data from CSV into dataframe
### 3. Writing common functions to render bar and count plot
### 4. Data cleaning
        a. Check if duplicate rows are there, if yes we could delete them but here we found none in this data set.
        b. Remove columns with NA, where all the values are NA 
        c. Finding out columns with only single value, for this analysis we could remove such columns as these would be of no help.
        d. Finding out columns that have more than 65% NA values, we can safely drop them.
        e. Dropping additional columns, which are of not much use in our analysis
        f. cleaning up numerical columns and removing the non digit values like text, % etc
        g. treating missing values 
            g. by updating the mode value to the missing values
            g. dropping rows as the values couldn't be assigned
            g. cleaning data by comibing the verification status 
            g. removing rows with the loan status as current as, we can't predict or do anything till the time loan is active to understand the behaviour
        h. checking outliers and keeping the values lesser than 99th percentile for the 'annual_inc' column rest columns seems to be rightly distributed
        i. derived column
            i. creating year and month columns to check the pattern of loans per year later
            i. creating buckets for annual income
            i. creating buckets for loan amount
            i. creating buckets for interest rates
### 5. Important variables on which we would run Univariate and Bivariate analysis
        1. Categorical variables
            1. Ordered categorical data
                1. grade
                2. sub_grade
                3. emp_length
                4. term
                5. issue_year
                6. issue_month
    
            2. Unordered categorical data
                1. addr_state
                2. home_ownership    
                3. purpose
                4. verification_status          
                    
        2. Quantitative variables
            1. annual_inc_bucket
            2. int_rate_bucket
            3. loan_amnt_bucket
### 6. Multivariate Analysis
        ## Correlation Metrics Insights
        Installment has a strong correlation with loan_amnt, funded_amnt, and annual income.
        term` has a good correlation with interest rate
        
        
        Employment length has a very weak correlation with most of the parameters.
        Issues month and year also have no correlation with any parameter.

### 7. Summary of Analysis   
        1. Almost 14% of loans are charged off.
        2. Grade E, F, & G loans are the major defaulters and have been correctly graded. Grades are the strongest predictor of the default. 
        3. Grade A has the least defaulters but still got some defaulters; grading could be done better to minimize the defaulters in Grade A to avoid business losses.
        4. Loans with subgrades of F and G are the major defaulters.
        5. Employment length has no impact on the defaulting, and we can see across the range of the experience that people are defaulting.
        6. A loan with the longer term has almost double the chance of defaulting compared to a short term; the company should promote short-term goals.
        7. Given numbers of loans were less in 2007, almost 29% got charged off.
        8. February is the month where the least number of loans has been issued; this is in sync with the financial year cycle, because of March being the financial year end. This makes sense, and the last quarter of the year has the least number of loans issued.
        9. WY state has the least defaulters, and NY has the maximum; this could also be because NY is the financial capital, and more loans are issued in NY; hence, more defaulters. CA has the maximum loans but average defaulters.
        10. Home ownership is not a strong parameter to determine the defaulter.
        11. Small businesses have seen the maximum defaulters; hence, the company should do more due diligence before giving loans in this sector. Bigger purchases seem to have minimum defaulters; it could also mean people with higher incomes doing those purchases and paying up the loans in time.
        12. Surprisingly, verified loans have defaulted more, which is serious, and the company could do better here and make the verification process work in favor of the company by avoiding bad loans; this could also indicate corruption in the verification process.
        13. People with higher annual incomes seem to be doing better, and companies should target loans to such profiles.
        14. The highest interest rate loans are defaulting more; this makes sense, as usually not-so-good credit score profiles get loans at higher interest rates and get defaulted. The company could avoid such loans and make the best of the loans where interest rates are lowest.
        15. Bigger loans seem to be defaulting more; the company can do more scrutiny here and try to bring down the loan amount for better outcomes for the company.
        16. People with the maximum income are going for the maximum loans, which is good for the company as they default less.
        


