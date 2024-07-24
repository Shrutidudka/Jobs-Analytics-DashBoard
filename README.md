# Jobs-Analytics-DashBoard
STEPS OF DATA SCRAPPING FROM THE LINKEDIN WEBSITE

Setting Up: The code imports libraries to control a web browser and work with data. It stores your LinkedIn username and password. It sets up a tool to control the Chrome web browser.

Logging In: The code opens the LinkedIn website. It waits for the login page to load and then types your username and password. It clicks the login button and waits for the main LinkedIn page to load.

Preparing for Data Collection: The code creates a container to store job information (designation, company, etc.). It identifies all the page numbers on the current job listings page (assuming they have a specific class name).

Looping Through Job Listing Pages: The code loops through each page number, potentially scraping jobs from all available pages. On each page, it clicks the corresponding page number to navigate. It waits a few seconds (not ideal) to allow the page to load. The code then identifies all the job listings on the current page (assuming they have a specific class name).

Extracting Data from Each Job Listing: The code loops through each job listing on the current page. For each job listing, it clicks on it to open the details page. It scrolls down the page to the bottom. The code then tries to extract various details about the job and company from the page:

Job title (designation) Company name Company size (number of employees) Company followers on LinkedIn Job seniority level Number of applicants (might be inaccurate) Job location!

Job title (designation)
Company name
Company size (number of employees)
Company followers on LinkedIn
Job seniority level
Number of applicants (might be inaccurate)
Job location
Storing Extracted Data: If the code successfully finds each data element, it stores the information in the container created earlier.

Overall, this code automates logging into LinkedIn and scraping data from job listings across potentially multiple pages.

Here the code file link :codeforwebscraping.ipynb

Dashboard 2

er diagram final

STEPS FOR DATA CLEANING :

Concatenation of Data: Combined multiple CSV files into a single DataFrame using pandas' concat() function. This step ensured that all relevant data is consolidated into a single structure for uniform analysis.

Renaming Columns: Standardized column names to ensure consistency. For example, changed all column names to have the to respective requirement.

Creating Unique Identifiers: Generated unique values for job_id, company_id, and details_id columns to uniquely identify each job, company, and job details.

Converting 'LinkedIn Followers' to Numbers: Processed the 'LinkedIn Followers' column to extract numerical values and convert them to integers. This involved removing any non-numeric characters, such as commas and text, using string replacement and type conversion.

Processing 'Employee Count': Similar to the 'LinkedIn Followers' column, cleaned the 'Employee Count' column by removing non-numeric characters and converting the values to integers for consistent numerical analysis.

Extracting Strings from 'Total Applicants': Extracted the relevant numerical data from the 'Total Applicants' column, which contained strings with multiple pieces of information. This was achieved using regular expressions and string manipulation to isolate the number of applicants.

Cleaning the 'Industry' Column: Processed the 'Industry' column to extract only the industry name, removing any additional information like employee counts or other descriptors.

Standardizing the 'Level' Column: Cleaned the 'Level' column to standardize the job level descriptions. Extracted specific keywords like 'Full-Time', 'Internship', and 'Mid-Senior level', ensuring that only these relevant terms were retained.

Checking for Duplicates: Identified and removed any duplicate rows in the DataFrame to maintain data integrity and prevent redundancy.

Handling Missing Values: Checked for null values across all columns. Rows with missing values were removed to ensure completeness and reliability of the data.

Separating DataFrames: Separated the cleaned DataFrame into three distinct tables: jobs, company, and details. This was done based on the specific attributes relevant to each table.

Saving Cleaned Data to CSV: Saved the cleaned and separated DataFrames into individual CSV files for further analysis and usage. This ensured that each table (jobs, company, details) was stored in a structured format for easy access and analysis.

Dashboard 2

Pinterest-Pioneers_074/README.md at
