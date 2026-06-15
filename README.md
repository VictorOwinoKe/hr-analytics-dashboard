# HR Analytics Dashboard

## Project Overview

This project is an interactive **Human Resources Dashboard** designed to help HR managers analyze workforce data from both a high-level summary perspective and a detailed employee-record perspective.

The dashboard provides insights into employee hiring trends, active and terminated employees, workforce demographics, salary distribution, education levels, performance ratings, and departmental salary patterns. It also includes a detailed employee records view that allows users to filter and explore individual employee information.

The project uses a realistic synthetic HR dataset containing **8,950 employee records**, generated using Python.

---

## User Story

As an HR manager, I want a comprehensive dashboard to analyze human resources data, providing both summary views for high-level insights and detailed employee records for in-depth analysis.

---

## Dashboard Views

The dashboard is divided into two main views:

1. **Summary View**
2. **Employee Records View**

---

## 1. Summary View

The Summary View provides high-level insights into the organization’s workforce. It is divided into three main sections:

* Overview
* Demographics
* Income Analysis

---

### Overview

The Overview section provides a snapshot of key HR metrics, including:

* Total number of hired employees
* Total number of active employees
* Total number of terminated employees
* Hiring and termination trends over the years
* Employee distribution by department
* Employee distribution by job title
* Employee comparison between headquarters and branch locations
* Employee distribution by city and state

In this dataset, **New York is considered the company headquarters**, while all other locations are treated as branch offices.

---

### Demographics

The Demographics section provides insights into the composition of the workforce, including:

* Gender ratio across the company
* Employee distribution by age group
* Employee distribution by education level
* Total employees within each age group
* Total employees within each education level
* Relationship between education level and performance rating

This section helps HR managers understand workforce diversity, age distribution, education patterns, and how education may relate to employee performance.

---

### Income Analysis

The Income Analysis section focuses on salary-related insights, including:

* Salary comparison across education levels
* Salary comparison by gender
* Salary trends by age and department
* Identification of salary discrepancies or patterns
* Relationship between employee age and salary within each department

This section supports compensation analysis and helps identify potential pay gaps or salary distribution patterns.

---

## 2. Employee Records View

The Employee Records View provides a detailed list of all employees in the dataset.

Each employee record includes key attributes such as:

* Employee ID
* First Name
* Last Name
* Gender
* State
* City
* Hire Date
* Department
* Job Title
* Education Level
* Performance Rating
* Overtime Status
* Salary
* Birth Date
* Termination Date
* Adjusted Salary

Users can filter the employee list based on available columns such as department, job title, gender, education level, location, performance rating, and employment status.

---

## Dataset

The dataset was synthetically generated using Python and contains **8,950 employee records**.

The goal of the dataset is to simulate realistic HR data that can be used for workforce analysis, dashboard development, and business intelligence reporting.

---

## Data Generation

The data generation process was designed to create realistic employee records using custom probability distributions and business rules.

The generated dataset includes the following fields:

| Column             | Description                                                          |
| ------------------ | -------------------------------------------------------------------- |
| Employee ID        | Unique identifier for each employee                                  |
| First Name         | Randomly generated employee first name                               |
| Last Name          | Randomly generated employee last name                                |
| Gender             | Randomly assigned gender with 46% Female and 54% Male distribution   |
| State              | Employee work location state                                         |
| City               | Employee work location city                                          |
| Hire Date          | Randomly generated hire date from 2015 to 2024                       |
| Department         | Employee department assigned using predefined probabilities          |
| Job Title          | Job title assigned based on department-specific probabilities        |
| Education Level    | Education level assigned based on job title requirements             |
| Performance Rating | Employee performance category                                        |
| Overtime           | Indicates whether the employee works overtime                        |
| Salary             | Base salary generated using department and job title salary ranges   |
| Birth Date         | Generated based on age group distribution and job title requirements |
| Termination Date   | Assigned to terminated employees based on termination rules          |
| Adjusted Salary    | Salary adjusted using gender, education, and age-based multipliers   |

---

## Data Generation Rules

The Python data generation script follows these rules:

* Generates **8,950 employee records**
* Assigns gender using a 46% Female and 54% Male probability
* Assigns employee locations from predefined states and cities
* Uses custom hire-date probabilities for each year between 2015 and 2024
* Assigns departments using predefined department probabilities
* Assigns job titles based on department-specific mappings
* Determines education level based on job title requirements
* Assigns performance ratings from:

  * Excellent
  * Good
  * Satisfactory
  * Needs Improvement
* Assigns overtime status using:

  * 30% Yes
  * 70% No
* Generates salary based on department and job title salary ranges
* Generates birth dates based on age group distribution and job requirements
* Assigns termination dates to approximately **11.2%** of employees
* Ensures termination dates occur at least six months after the hire date
* Calculates adjusted salary based on gender, education level, and age

---

## Key Business Questions

This dashboard helps answer important HR questions such as:

* How many employees are currently active?
* How many employees have been terminated?
* How have hiring and termination trends changed over time?
* Which departments have the highest number of employees?
* What job titles are most common across the company?
* How does employee distribution differ between headquarters and branches?
* What is the gender distribution across the workforce?
* Which age groups make up the largest share of employees?
* What education levels are most common among employees?
* Is there a relationship between education level and performance rating?
* Are there salary differences between genders across education levels?
* How does salary vary by age and department?
* Which departments have the highest salary ranges?

---

## Project Structure

```text
HR-Dashboard/
│
├── data/
│   └── hr_dataset.csv
│
├── scripts/
│   └── generate_hr_dataset.py
│
├── dashboard/
│   └── hr_dashboard_file
│
├── images/
│   └── dashboard_screenshots
│
└── README.md
```

---

## Tools and Technologies

This project can be developed using the following tools:

* **Python** for synthetic data generation
* **Pandas** for data manipulation
* **NumPy** for random data generation and probability-based sampling
* **Faker** for generating realistic employee names
* **Power BI, Tableau, or Looker Studio** for dashboard development
* **Excel or CSV** for storing and importing the dataset

---

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/hr-analytics-dashboard.git
cd hr-analytics-dashboard
```

### 2. Install Required Python Packages

```bash
pip install pandas numpy faker
```

### 3. Generate the Dataset

```bash
python scripts/generate_hr_dataset.py
```

This will generate a synthetic HR dataset and save it as a CSV file.

### 4. Load the Data into a BI Tool

Import the generated CSV file into your preferred dashboarding tool, such as Power BI, Tableau, or Looker Studio.

### 5. Build or Open the Dashboard

Use the dataset to create the Summary View and Employee Records View based on the requirements described above.

---

## Dashboard Features

### Summary Metrics

* Total hired employees
* Total active employees
* Total terminated employees
* Hiring trend by year
* Termination trend by year

### Workforce Breakdown

* Employees by department
* Employees by job title
* Employees by city
* Employees by state
* HQ vs branch comparison

### Demographic Analysis

* Gender distribution
* Age group distribution
* Education level distribution
* Education and performance relationship

### Income Analysis

* Salary by education level
* Salary by gender
* Salary by department
* Salary by age
* Salary comparison across demographic groups

### Employee Records

* Detailed employee-level table
* Filterable employee information
* Searchable and sortable records

---

## Insights Expected from the Dashboard

The dashboard is designed to help HR teams:

* Monitor workforce growth and attrition
* Understand employee demographics
* Identify hiring and termination trends
* Analyze compensation patterns
* Detect possible salary discrepancies
* Explore employee performance by education level
* Improve workforce planning and HR decision-making

---

## Future Improvements

Possible future enhancements include:

* Adding attrition prediction using machine learning
* Creating employee retention risk scores
* Adding department-level performance benchmarking
* Including diversity and inclusion metrics
* Adding salary band analysis
* Adding time-to-promotion analysis


---

## Disclaimer

This dataset is synthetically generated and does not represent real employees or any real organization. It is intended for portfolio, learning, and demonstration purposes only.

---

## Author

**Victor Owino**
Data Analyst | Business Intelligence | Data Science | AI and Analytics

Portfolio: [victorowino.com](https://victorowino.com)
