# SAP plus extend and innovate with Data and AI hands-on lab step-by-step

## Abstract and learning objectives

In this hands-on lab you will **extract** (historical) Sales Orders from SAP S/4 HANA and historical payments from a non-SAP system, in this case Cosmos DB using Azure Synapse Analytics pipelines. You will **visualize** the extracted Sales Orders and invoice data with Power BI. Next, you will unleash the power of data using Azure Machine Learning to train a model to **predict** incoming cash flow. You will learn to implement dashboards and alerting using Power BI and Power Automate. Finally, you will add the ability to update data in SAP based on insights gained from the prediction model.

## Overview

When customers buy goods, the corresponding payments are not completed immediately. Some customers will pay directly while other customers will pay at the end of their payment terms. This makes it difficult for companies to predict the incoming cashflow. In this lab, Azure tooling is used to predict the incoming cashflow. To predict cash flow, historical Sales Orders and payments data is required. Contoso Retail also needs a way to flag risky customers in the SAP system whose payments tend to arrive late.

## Solution architecture

![The solution architecture diagram displays as described below.](media/solution_architecture.png "Solution architecture")

 Sales Order information is stored in an S/4 HANA system and payments data is stored in Cosmos DB. Synapse Pipelines are used to ingest historical data from both sources. Power BI is used to visualize historical data and to create reports. Azure Machine Learning is used to create a model to predict incoming cash flow. Finally, a data alert is established to identify risky payers whose payments are typically late. This alert triggers a Power Automate process that will in-turn flag the risky payers in SAP.
