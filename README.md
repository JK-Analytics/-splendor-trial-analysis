# Splendor Analytics Trial Activation Analysis

## Overview
Analysis of behavioural data from Splendor Analytics' 30-day 
free trial to define Trial Activation and understand what 
drives conversion to paid customers.

## Key Findings
- Overall conversion rate: **21.3%** (1 in 5 orgs)
- **50.8%** of orgs show zero goal completion
- Activated orgs convert at **33.3%** vs 21.2% (1.57x lift)
- Scheduling dominates at **87.8%** module adoption
- **55.4%** of event timestamps were null (data quality issue)

## Trial Goals Defined
| Goal | Activity | Threshold |
|---|---|---|
| Goal 1 | Scheduling.Shift.Created | 3+ times |
| Goal 2 | Scheduling.Shift.Approved | 1+ times |
| Goal 3 | Scheduling.Template.ApplyModal.Applied | 1+ times |
| Goal 4 | Scheduling.OpenShiftRequest.Created | 1+ times |
| Goal 5 | PunchClock.PunchedIn | 1+ times |

## Project Structure
```
splendor-trial-analysis/
├── Data/
│   └── DA task.csv
├── notebooks/
│   ├── 01_cleaning_eda.ipynb
│   └── 03_descriptive_analytics.ipynb
├── SQL/
│   ├── Staging/
│   │   └── stg_events.sql
│   └── Marts/
│       ├── mart_trial_goals.sql
│       └── mart_trial_activation.sql
└── requirements.txt
```

## How To Run
1. Install dependencies:
```
pip install -r requirements.txt
```
2. Open Jupyter Notebook
3. Run `01_cleaning_eda.ipynb` first
4. Then run `03_descriptive_analytics.ipynb`

## Tools Used
- Python (pandas, numpy, matplotlib, seaborn, scikit-learn, scipy)
- SQL (DuckDB compatible)
- Jupyter Notebook
- Git & GitHub

## Author
John Kingsley Emeka
