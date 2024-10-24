# Proactive Maintenance Project

## Introduction
This project focuses on implementing proactive maintenance practices to prevent machine failures in industrial settings. The objective is to highlight the benefits of proactive maintenance strategies over reactive maintenance approaches, which are often employed after a failure occurs.

## Why Proactive Maintenance is Necessary
Proactive maintenance is crucial in industrial operations to ensure the reliability, safety, and efficiency of machinery. Unlike reactive maintenance, which only addresses issues once they occur, proactive maintenance involves regular monitoring and maintenance of equipment to prevent failures before they happen. Key reasons for adopting proactive maintenance include:

1. **Minimizing Downtime**: Proactive maintenance helps identify potential issues early, reducing unexpected machine breakdowns that can lead to costly downtimes.
2. **Cost Savings**: By addressing problems before they escalate into significant failures, companies save on repair costs, avoid emergency maintenance expenses, and reduce losses associated with production halts.
3. **Increased Equipment Lifespan**: Regular maintenance improves the durability and lifespan of machinery, ensuring long-term operational efficiency.
4. **Enhanced Safety**: Proactive measures help identify safety hazards associated with faulty equipment, thereby preventing accidents and ensuring a safer work environment.
5. **Efficient Resource Utilization**: Scheduling maintenance activities in advance allows for better planning of labor, tools, and spare parts, resulting in more efficient use of resources.

## Input Files
The dataset is obtained from Kaggle, which contains five `.csv` files describing different events (error, failure, and maintenance) and the sensor data for each machine.

## Approach
- **`convert.ipynb`**: Aggregated the hourly machine data into daily data over 24-hour periods. The original hourly data was imbalanced, with a higher frequency of non-failure entries compared to failure entries.
- **`mainmodel.ipynb`**: Developed an LSTM model to predict machine failures using time-series data on pressure, vibration, speed, and temperature. To handle data imbalance, I applied SMOTE, standardized the variables, and performed comprehensive data preprocessing. Additionally, I categorized the severity levels of the failures. The model achieved an F1 score of 0.97, indicating high accuracy in predicting and classifying failure severities.
- **`input.ipynb`**: Implemented a feature that takes user input regarding machine conditions. Based on this input, an automated email is sent to the user, specifying the detected type of machine failure and recommending appropriate preventive measures to mitigate the issue. This system helps provide users with timely guidance on addressing potential equipment failures.
- **`refresh.ipynb`**: Implemented a feature to collect user input regarding machine conditions and automatically store this information in a CSV file for record-keeping.