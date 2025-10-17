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

##  [View the coupon acceptance analysis notebook](prompt.ipynb)

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

### 3. Findings and conclusions

- Overall coupon acceptance rate: **56.84%**
- Bar coupons had lower acceptance: **41.00%**

**Bar Coupon Analysis**
   - Visit Frequency Matters Most
   - Drivers visiting bars 3 or fewer times/month: 37.07% acceptance
   - Drivers visiting bars more than 3 times/month: **76.88% acceptance** (2x higher)
   - Bar-goers (>1/month) over age 25: **69.52% acceptance**, All others: 33.50% acceptance,  Difference: 36.02 percentage points
   - Bar-goers (>1/month), no kids, non-farming occupation: **71.32% acceptance** while All others: 29.60% acceptance, Having kids as passengers drastically reduces bar coupon acceptance
   - Drivers meeting favorable conditions (frequent bar/restaurant visits, younger age, no kids): **58.89% acceptance** while Drivers not meeting these conditions: 29.81% acceptance
   - Younger drivers (age 20) highest acceptance (63.44%), decreases with age
   - Occupation Healthcare Support (69.83%) and Construction (68.83%) highest; Retired (45.86%) and Legal (47.03%) lowest


### Conclusions

 - Drivers who regularly visit a venue type are 2x more likely to accept related coupons
 - Passenger type (especially having children) significantly impacts acceptance, particularly for bar coupons
 - Acceptance rates decline with age, with under-30 drivers showing highest engagement


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
