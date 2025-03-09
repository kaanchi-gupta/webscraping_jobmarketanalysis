# Data Analytics Job Market Analysis - Web Scraping & Insights

## Overview  
This project focuses on **web scraping job listings** for Data Analytics roles using **Selenium**. I extracted job titles, company names, locations, job types, and salary ranges from SimplyHired to analyze salary distributions and hiring trends.

## Challenges Faced & Fixes  

1. **Website Blocking & CAPTCHAs**  
   - Some sites detected automation, so I switched to a scrape-friendly job portal.  

2. **Dynamic Page Loading Issues**  
   - Used `WebDriverWait` to ensure elements were fully loaded before extraction.  

3. **Data Extraction Errors**  
   - **Company Names Missing**: Adjusted XPath selectors to correctly extract employer names.  
   - **Job Location Extraction**: Ensured the right HTML elements were targeted to capture city/state info.  
   - **Salary Formatting Issues**:  
     - Converted "95.8K" to "95,800" to ensure accurate numerical representation.  
     - Removed "Estimated:" text to extract clean salary values.  

4. **Inconsistent Job Details Structure**  
   - Some job postings did not list salaries, so missing values were handled as "Not Provided."  
   - Job type (Full-time/Part-time) was mixed with salary details, so I split them into separate columns.  

5. **Data Cleaning & Visualization Issues**  
   - Filtered out unrealistic salary values (e.g., below $20,000).  
   - Adjusted bin sizes in histograms to avoid distorted distributions.  
   - Ensured company analysis only included valid employers (not "Not Listed").  

## Key Analyses Conducted  

- **Top Hiring Companies** – Identifying companies with the highest number of job postings.  
- **Salary Distribution** – Analyzing the common salary ranges in Data Analytics roles.  
- **Highest-Paying Companies** – Determining which firms offer the best max salaries.  

This project provides a structured analysis of the Data Analytics job market, offering insights into salary expectations and hiring trends.  
