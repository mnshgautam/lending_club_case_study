# lending_club_case_study

## Steps performed
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
### 7. Summary of Analysis   
