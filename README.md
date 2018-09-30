# Sensors_Data - User-behavior Analytics and Conversion Prediction

<img src="https://github.com/will-zw-wang/Sensors_Data-User_Behavior_Analytics_and_Conversion_Prediction/blob/master/images/Sensors_Data_Image.jpg">

## Project Objectives

Sensorsdata is a leading China-based and rapidly growing big data company and interested in User-behavior Analytics and Conversion Prediction. To help explore this question, they have provided log data containing tens of thousands of log information of Sensorsdata main webpage for a week. 

## Dataset Description

Data is given as txt file whereas data is in JSON format. Dataset contains cache log information of Sensorsdata main webpage for a week, including actions on leaving the webpage, click a button, send verification code, apply for account, etc.   
Log Description for detailed description please refer to: https://github.com/will-zw-wang/Sensors_Data/tree/master/log_description

## Analysis Structure

1. Log Data Processing
2. EDA


## Analysis Details

### 1. Log Data Processing
- Identify types of events
- Identify properties of events
- Select related properties to generate Dataframe
- Details please refer to: https://github.com/will-zw-wang/Sensors_Data-User_Behavior_Analytics_and_Conversion_Prediction/blob/master/code/Log%20Data%20Processing.ipynb

### 1. EDA
- Select identifier
- Numeric variables
  - **page_stayTime**: 
    - Insights: Only 11.41 % of the people who clicked the functional pages stayed more than 3 seconds
    - Create feature "page_stayTime": Sum up the total stay time by pages.
- Categorical variables
  - **event**: 
    - Insights: Most users did not attempt to submit a form
    - Sign_up Funnel: page view(32620) -> btnClick(13866) -> click_send_cellphone(600) -> verify_cellphone_code(563) -> clickSubmit(513) -> formSubmit(791)
  - **day**: 
    - Insights: 2017-03-11 and 2017-03-12 are weekends and have the least number of counts, perhaps users visit our website more for work purposes.
    - Create feature 'weekend': Values: '1' for weekend, '0' and weekdays
  - **title**:
    - Insights: 
      - Users visit our ‘demo’ page, ‘user manual’ page and ‘product’ page most frequently. 
      - If we plan to improve the layout of our pages, these three pages should have high priority.
  - **latest_referrer_host**:
    - Insights: 
      - Most of empty ‘latest_referrer_host’ are directly from sensordata website. 
      - The other users were referred mostly from 'baidu', '36kr', 'sogou' and 'google', especially 'baidu' which contributed times of referred users than the other hosts. 
      - Thus, if we want to run marketing campaign, 'baidu' should be allocated more budget to.
    - Create feature 'latest_referrer_host_bin': With values: 'sensordata', 'baidu' and 'others'

- Select features
