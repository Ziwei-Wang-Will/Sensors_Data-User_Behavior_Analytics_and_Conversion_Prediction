# Sensors_Data

<img src="https://github.com/will-zw-wang/Sensors_Data-User_Behavior_Analytics_and_Conversion_Prediction/blob/master/images/Sensors_Data_Image.jpg">

## Project Objectives

Sensorsdata is a leading China-based and rapidly growing big data company and interested in User-behavior Analytics and Conversion Prediction. To help explore this question, they have provided log data containing tens of thousands of log information of Sensorsdata main webpage for a week. 

## Dataset Description

Data is given as txt file whereas data is in JSON format. Dataset contains cache log information of Sensorsdata main webpage for a week, including actions on leaving the webpage, click a button, send verification code, apply for account, etc.   
Please refer to Log Description for detailed description: https://github.com/will-zw-wang/Sensors_Data/tree/master/log_description

## Analysis Structure

1. Log Data Processing
2. 


## Analysis Details

### 1. Log Data Processing

- Funnel Analysis:
page view(32620) -> btnClick(13866) -> click_send_cellphone(600) -> verify_cellphone_code(563) -> clickSubmit(513) -> formSubmit(791)
It seems that most users did not attempt to submit a form
