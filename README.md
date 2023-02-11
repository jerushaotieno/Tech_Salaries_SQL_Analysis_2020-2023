# Tech_Salaries_SQL_Analysis_2020-2023

Tech_Salaries_SQL_Analysis_2020-2023 is a SQL analysis of salary data between 2020 and 2023 for techies working for US-based companies. The goal is to understand the distribution of salaries across different variables such as job title, experience level, remote work, company size, employment type, location, currency, and time. By conducting these analyses, a business could gain insights into various factors that may impact salary and make data-driven decisions to improve compensation policies or make other strategic decisions. Additionally, the analysis can be used to identify any potential disparities in salary and to make recommendations for addressing any inequalities.

For example, the results of the "Experience Level vs Salary" analysis indicates that there is a correlation between experience level and salary, and the business could use this information to make decisions about how to structure compensation for employees at different experience levels. By grouping the data by employment type and calculating the average salary for each group, the business can compare the salary of different employment types. Similarly, the "Salary Trends over time" analysis provides insight into how salaries have changed over time and could inform decision-making about compensation policies and strategies.

# Dataset Details 

This database was sourced from https://ai-jobs.net/salaries/download/

It contains 11 columns and 2,638 rows of data.

The dataset basically contains a single table with all salary information structured as follows:

### work_year   

The year the salary was paid.

### experience_level    

The experience level in the job during the year with the following possible values:
    EN    Entry-level / Junior
    MI    Mid-level / Intermediate
    SE    Senior-level / Expert
    EX    Executive-level / Director

### employment_type
 
 The type of employement for the role:
    PT    Part-time
    FT    Full-time
    CT    Contract
    FL    Freelance

### job_title

The role worked in during the year.

### salary

The total gross salary amount paid.

### salary_currency

The currency of the salary paid as an ISO 4217 currency code.

### salary_in_usd

The salary in USD (FX rate divided by avg. USD rate of respective year via data from BIS).

### employee_residence

Employee's primary country of residence in during the work year as an ISO 3166 country code.

### remote_ratio

The overall amount of work done remotely, possible values are as follows:
    0     No remote work (less than 20%)
    50    Partially remote
    100   Fully remote (more than 80%)

### company_location

The country of the employer's main office or contracting branch as an ISO 3166 country code.

### company_size

The average number of people that worked for the company during the year:
    S   less than 50 employees (small)
    M   50 to 250 employees (medium)
    L   more than 250 employees (large)
    
# SQL Analysis Details 

### Salary Distribution among different job titles and experience levels
-- Shows the average salary for each group

[Salary Distribution among different job titles and experience levels.csv](https://github.com/jerushaotieno/Tech_Salaries_SQL_Analysis_2020-2023/files/10714340/Salary.Distribution.among.different.job.titles.and.experience.levels.csv)

### Relationship between remote work and salary
-- Shows the average salary for each unique value of remote_ratio -- Remote ratio of 0 gives the highest average salaries while that of 50 gives the least average salaries -- Remote ratio of 0 has an average salary of USD 139,537.677364865 -- Remote ratio of 100 has an average salary of USD 134,422.291731669 -- Remote ratio of 50 has an average salary of USD 78,025.9069767442


[Relationship between remote work and salary.csv](https://github.com/jerushaotieno/Tech_Salaries_SQL_Analysis_2020-2023/files/10714346/Relationship.between.remote.work.and.salary.csv)

### Relationship between company size and salary
-- Shows the average salary for each unique value of company_size
-- The average salaries for those is medium-sized companies is the highest while the least average salaries are for those in small-sized companies
-- Average salary for techies in small-sized companies is USD 77,665.8106060606
-- Average salary for techies in large-sized companies is USD 112,580.023560209
-- Average salary for techies in medium-sized companies is USD 140,162.423728814

[Relationship between company size and salary.csv](https://github.com/jerushaotieno/Tech_Salaries_SQL_Analysis_2020-2023/files/10714349/Relationship.between.company.size.and.salary.csv)

### Salary by employment type
-- Shows the average salary for each unique value of employment_type
-- Techies on contract earn the most followed by those on full-time employment. Part-time techies earn the least.
-- Average salary for techies on contract is USD 134,871.125
-- Average salary for freelance techies is USD 52,259.75
-- Average salary for part-time techies is USD 39,865.125
-- Average salary for full-time techies is USD 133,855.546815042

[Salary by employment type.csv](https://github.com/jerushaotieno/Tech_Salaries_SQL_Analysis_2020-2023/files/10714350/Salary.by.employment.type.csv)

### Salary by location
-- Shows the average salary for each unique value of employee_residence and company_location 

[Salary by location.csv](https://github.com/jerushaotieno/Tech_Salaries_SQL_Analysis_2020-2023/files/10714351/Salary.by.location.csv)

### Experience level vs salary
-- Shows the average salary for each unique value of experience_level
-- Executive-level techies earn the most followed by senior-level ones. The least earners are entry-level techies.
-- The average salary for Mid-level / Intermediate techies is USD 99,883.6738056013
-- The average salary for Senior-level / Expert techies is USD 150,562.579069767
-- The average salary for Executive-level / Director techies is USD 196,640.581081081
-- The average salary for Entry-level / Junior techies is USD 70,945.2109704641

[Experience level vs salary.csv](https://github.com/jerushaotieno/Tech_Salaries_SQL_Analysis_2020-2023/files/10714352/Experience.level.vs.salary.csv)

### Salary trends over time
-- Shows the average salary for each unique value of work_year
-- Salaries for techies have been increasing since 2020. They are earning the highest in 2023. 
-- The biggest leap in salary increment took place in 2022, up from 2021.
-- The average salary in 2023 is USD 149,748.241581259
-- The average salary in 2022 was USD 133,448.083030303
-- The average salary in 2021 was USD 93,456.7739130435
-- The average salary in 2020 was USD 93,333.3333333333
 
[Salary trends over time.csv](https://github.com/jerushaotieno/Tech_Salaries_SQL_Analysis_2020-2023/files/10714353/Salary.trends.over.time.csv)
