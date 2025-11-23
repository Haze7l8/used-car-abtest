
# Used Car Market A/B Test Analysis

## Project Overview
This project analyzes 400,000+ used car listings to evaluate the impact of a website redesign using an A/B test framework.
The analysis focuses on differences in price, vehicle age, brand distribution, and transaction duration between the test and control groups.
The goal is to determine whether the new website version improves user experience and enhances transaction efficiency.

## Dataset Description
The dataset includes key fields such as:
price – listed selling price
yearOfRegistration / monthOfRegistration – registration year/month
dateCreated – date the listing was created
lastSeen – last time the listing was online
vehicleType / brand / model
fuelType, gearbox
abtest – assignment to test or control group
Total variable: 20
Total records: ~400,000 rows

## Tools & Technologies
| Category |	Tools |
|---------|----------|
| Language |	Python |
| Data Processing	| Pandas, NumPy |
| Statistical Analysis	| SciPy |
| Visualization	| Matplotlib, Seaborn |
| Environment	| Jupyter Notebook |

## Data Cleaning & Preprocessing
Main steps:
Removed invalid prices (price = 0 or extremely high outliers)
Converted all date columns to datetime format
Created vehicle age feature from registration year
Generated duration feature = lastSeen - dateCreated
Verified A/B group overlap and removed pre-experiment data
Filtered anomalies in mileage and power fields
Ensured test/control groups are comparable

## Exploratory Data Analysis (EDA)
Performed the following analyses:
Price distribution (histogram, KDE)
Vehicle age & mileage distributions
Boxplots comparing test vs control
Correlations between price, age, power
Outlier inspection
Key visualizations are included in the notebook.

## A/B Test Methodology
Applied statistical tests using SciPy:
| Metric | Test | Purpose |
|---------|----------|----------|
|Price	|t-test	|Check if redesign affects pricing|
|Vehicle age	|t-test	|Check quality consistency|
|Brand share	|Chi-square	|Compare brand distributions|
|Duration	|t-test	|Evaluate transaction speed|

Significance level: α = 0.05

## Key Results

### Price
p = 0.20 → No significant difference
Redesign does not affect selling price.

### Vehicle Age
p = 0.52, both groups ~ 12.9 years old
Vehicle quality remains stable.

### Brand Distribution
p = 0.93
No structural change in listed brands.

### Transaction Duration
p = 0.047 < 0.05 → Significant
New website reduces time from listing to deal, improving efficiency.

## Conclusion
The redesign does not change the quality or type of vehicles published.
Transaction speed significantly improves, indicating a better user experience.
Recommendation: Continue rollout of redesigned interface.

## Project Files
a-b-test-of-used-cars.ipynb — Complete analysis, code & charts

## Notebook Link
https://github.com/Haze7l8/used-car-abtest/blob/46b2f514a85bd5bba926ff8f311c3bbbb2a32606/a-b-test-of-used-cars.ipynb

## Author
Zhenyao Xu
