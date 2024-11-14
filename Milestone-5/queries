-- Question 1: What is the gender distribution of respondents from India?
SELECT gender, COUNT(*) AS count FROM dataset WHERE country = 'In' GROUP BY gender;

-- 2. What percentage of respondents from India are interested in education abroad and sponsorship?
SELECT higher_study_aspiration, count(higher_study_aspiration), (COUNT(*) * 100.0 / (SELECT COUNT(*) FROM dataset WHERE country = 'In')) AS percentage FROM dataset WHERE country = 'In' group by higher_study_aspiration;

-- Question 3: What are the 6 top influences on career aspirations for respondents in India?
SELECT influencing_factor, COUNT(*) AS count FROM dataset WHERE country = 'In' GROUP BY influencing_factor ORDER BY count DESC LIMIT 6;

-- Question 4: How do career aspiration influences vary by gender in India?
SELECT gender, influencing_factor, COUNT(*) AS count FROM dataset WHERE country = 'In' GROUP BY gender, influencing_factor;

-- 5. What percentage of respondents are willing to work for a company for at least 3 years?
SELECT 3yr_tenurity, count(3yr_tenurity),(COUNT(*) * 100.0 / (SELECT COUNT(*) FROM dataset)) AS percentage FROM dataset WHERE 3yr_tenurity = 'yes' group by 3yr_tenurity;

-- 6. How many respondents prefer to work for socially impactful companies?
SELECT No_Mission_vote, COUNT(*) AS count FROM dataset group by No_Mission_vote;

-- 7. How does the preference for socially impactful companies vary by gender?
SELECT gender, No_Mission_vote, COUNT(No_Mission_vote) FROM dataset group by gender, No_Mission_vote;

-- 8. What is the distribution of minimum expected salary in the first three years among respondents?
SELECT min_salary_3yr, COUNT(min_salary_3yr) AS count FROM dataset GROUP BY min_salary_3yr;

-- 9. What is the expected minimum monthly salary in hand?
SELECT min_start_salary, avg(min_start_salary) FROM dataset group by min_start_salary order by min_start_salary DESC LIMIT 1;

-- 10. What percentage of respondents prefer remote working?
SELECT WFH_vote, (COUNT(*) * 100.0 / (SELECT COUNT(WFH_vote) FROM dataset)) AS percentage FROM dataset group by WFH_vote;

-- 11. What is the preferred number of daily work hours?
SELECT working_hours, COUNT(working_hours) FROM dataset GROUP BY working_hours;

-- 12. What are the common work frustrations among respondents?
SELECT frustration_reason, COUNT(frustration_reason) AS count FROM dataset GROUP BY frustration_reason ORDER BY count DESC;

-- 13. How does the need for work-life balance interventions vary by gender?
SELECT gender, full_break_frequency, COUNT(full_break_frequency) AS count FROM dataset GROUP BY gender,full_break_frequency;

-- 14. How many respondents are willing to work under an abusive manager?
SELECT work_under_abusive_manager, COUNT(work_under_abusive_manager) AS count FROM dataset WHERE work_under_abusive_manager = 'Yes';

-- 15. What is the distribution of minimum expected salary after five years?
SELECT min_salary_5yr, COUNT(min_salary_5yr) AS count FROM dataset group by min_salary_5yr;

-- 16. What are the remote working preferences by gender?
SELECT gender, WFH_vote,COUNT(WFH_vote) AS count FROM dataset GROUP BY gender, WFH_vote;

-- 17. What are the top work frustrations for each gender?
SELECT gender, frustration_reason, COUNT(frustration_reason) AS count FROM dataset GROUP BY gender,frustration_reason ORDER BY gender, count DESC;

-- 18. What factors boost work happiness and productivity for respondents?
SELECT happy_productive_reason, COUNT(happy_productive_reason) AS count FROM dataset GROUP BY happy_productive_reason ORDER BY count DESC;

-- 19. What percentage of respondents need sponsorship for education abroad?
SELECT higher_study_aspiration, (COUNT(*) * 100.0 / (SELECT count(higher_study_aspiration) FROM dataset)) AS percentage FROM dataset WHERE higher_study_aspiration = 'sponsor';
