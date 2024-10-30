# DataUnderstanding_Python_DataWrangling
Check out the code file attached or view it at the given link: [Click here](https://colab.research.google.com/drive/1ofKGUN907pP6JJpy6eWAq6wIOGYebj0F?usp=sharing)
## Introduction
### 1. Business Question:
**This project focuses on analyzing transaction and payment data for an e-wallet company**. The analysis is divided into two main parts: **Exploratory Data Analysis (EDA) and Data Wrangling**. The datasets used include payment_report.csv, product.csv, and transactions.csv, each providing essential insights into the company's performance, product offerings, and transaction behaviors.
### 2. Dataset:
transaction.csv
|Variable|Description|
|-|-|
|transaction_id|Unique identifier for each transaction.|
|merchant_id|ID of the merchant involved in the transaction.|
|volume|The monetary amount of the transaction.|
|transType|Code representing the type of transaction (e.g., payment, withdrawal).|
|transStatus|Status code indicating the success or failure of the transaction.|
|sender_id|ID of the sender initiating the transaction.|
|receiver_id|ID of the receiver for the transaction.|
|extra_info|Additional information related to the transaction, if applicable.|
|timeStamp|Timestamp indicating the time when the transaction occurred.|

product.csv
|Variable|Description|
|-|-|
|product_id|Unique identifier for each product.|
|category|Category code or name representing the type of product.|
|team_own|Team responsible for the product.|

payment_report.csv
|Variable|Description|
|-|-|
|report_month|Month and year for the payment report (e.g., "2023-01" for January 2023).|
|payment_group|Group type of the payment, such as "payment" or "refund."|
|product_id|ID of the product involved in the payment transaction.|
|source_id|ID representing the source of the transaction.|
|volume|Total transaction volume for the given product and source in the specified month.|  

## Process:
### Part I: Exploratory Data Analysis (EDA)
In this phase, the data is explored and cleaned by identifying:

- **Missing Data**: Report on rows with missing values, including suggested actions (e.g., deletion, imputation).
- **Duplicates**: Check for duplicate records and define next steps.
- **Incorrect Data Types**: Identify columns with incorrect data types and propose corrections.
- **Incorrect Values**: Highlight any incorrect values found in the datasets with suggested resolutions.

### Part II: Data Wrangling and Insights
This section involves in-depth analysis and wrangling of the datasets to derive key insights:

- **Top Products**: Identify the top 3 product IDs with the highest payment volume.
- **Abnormal Product Ownership**: Determine if there are any products that violate the rule of one product ID being owned by a single team.
- **Team Performance**: Analyze performance metrics to find the team with the lowest payment volume since Q2 2023 and identify the category contributing the least to that team's performance.
- **Refund Transaction Analysis**: Examine the contribution of source IDs related to refund transactions to find which source ID has the highest contribution.
- **Transaction Type Definition**: Classify each transaction in the transactions.csv dataset based on defined criteria (e.g., Bank Transfer, Withdraw Money, etc.) and identify invalid transactions.
- **Transaction Metrics**: For each valid transaction type, calculate the number of transactions, total volume, senders, and receivers.

## Conclusion:
The analysis of the payment and transaction datasets provides valuable insights into the e-wallet company’s operations.

### Exploratory Data Analysis (EDA) Results
From the EDA of payment_report.csv and product.csv, it was identified that **2% (22 rows) of the category and team_own columns contained missing data** due to some Product IDs in the payment report not existing in the product dataset. However, **no action is needed as this does not significantly impact the analysis**. Notably, there were n**o duplicates, incorrect data types, or incorrect values in these datasets, indicating a clean dataset for further analysis.**

In the transactions.csv dataset, **missing data was identified in the sender_id, receiver_id, and extra_info** columns. While **no immediate action is required**, this could be addressed in future analyses to enhance data quality. T**he dataset contained 28 duplicate rows**, which will **be deleted to ensure accuracy in subsequent calculations**. Again, there were **no issues with incorrect data types or values**.

### Key Findings from Data Wrangling
**Top Products:** The analysis revealed that the top three product IDs with the highest transaction volume were 1976, 429, and 372. This insight can help prioritize product marketing and resource allocation.

**Abnormal Product Ownership:** The review of product ownership highlighted anomalies with product IDs 3, 1976, and 10033, which do not conform to the rule of single-team ownership. This could warrant further investigation to clarify ownership structures.

**Team Performance:** The team identified with the lowest performance since Q2 2023 was APS, with their least productive category being PXXXXXE. This finding suggests potential areas for improvement and targeted strategies to enhance team performance.

**Refund Transaction Insights:** The analysis of refund transactions indicated that the source ID contributing the most was 38, with a substantial volume of 36,527,454,759. Understanding the sources of refunds can inform strategies to minimize future occurrences and enhance customer satisfaction.

**Overall Implications**
These findings highlight critical aspects of product performance, team accountability, and transaction dynamics within the e-wallet service. Addressing the identified issues and leveraging the insights gained will enable the company to enhance operational efficiency, optimize product offerings, and improve overall financial performance.


