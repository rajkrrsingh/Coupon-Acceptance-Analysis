# Coupon Acceptance Analysis

## Overview
Analysis of customer behavior regarding driving coupons using data from Amazon Mechanical Turk survey. This project explores factors that influence whether drivers accept coupons for bars, restaurants, and coffee houses.

## Dataset
- **Source**: Amazon Mechanical Turk survey
- **Size**: 12,684 observations
- **Features**: 
Data columns (total 25 columns):
 #   Column                Non-Null Count  Dtype 
---  ------                --------------  ----- 
 0   destination           12684 non-null  object
 1   passanger             12684 non-null  object
 2   weather               12684 non-null  object
 3   temperature           12684 non-null  int64 
 4   time                  12684 non-null  object
 5   coupon                12684 non-null  object
 6   expiration            12684 non-null  object
 7   gender                12684 non-null  object
 8   age                   12684 non-null  object
 9   maritalStatus         12684 non-null  object
 10  has_children          12684 non-null  int64 
 11  education             12684 non-null  object
 12  occupation            12684 non-null  object
 13  income                12684 non-null  object
 14  Bar                   12577 non-null  object
 15  CoffeeHouse           12467 non-null  object
 16  CarryAway             12533 non-null  object
 17  RestaurantLessThan20  12554 non-null  object
 18  Restaurant20To50      12495 non-null  object
 19  toCoupon_GEQ5min      12684 non-null  int64 
...
 23  direction_opp         12684 non-null  int64 
 24  Y                     12684 non-null  int64 

## Key Findings - Bar Coupons

### 1. Frequency is the Strongest Predictor
- Drivers who visit bars **>3 times/month**: **76.17%** acceptance rate
- Drivers who visit bars **≤3 times/month**: **37.27%** acceptance rate
- **39% difference** - existing habits strongly predict coupon acceptance


### 2. Key Hypothesis
**Coupons reinforce existing behavior rather than create new behavior.** 
1. people who are going to bar are more likely accept the coupons.
2. drivers going bar more than 1 times in a month and above age of 25 has high rate of acceptance rate.
3. cost consious driver are more likely to accept coupons.
4. drivers having non-farming occupations are are most likely accept the coupons.
5. driver who never go to bars are least likely accept the coupons.



## Tech Stack and libraries
- Python 3.13
- pandas, numpy, matplotlib, seaborn

## How to Run
```bash
# Activate virtual environment
python3 -m venv venv && source venv/bin/activate
pip3 install matplotlib seaborn pandas numpy jupyter
# Launch Jupyter notebook
jupyter notebook prompt.ipynb
```
