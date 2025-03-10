# Domain-Case-Study-BFSI-Home-Credit-Assignment

Overview

This assignment involves working with real-world application and bureau data shared by Home Credit. The objective is to practice the end-to-end process of model development in Credit Risk for Banks, Financial Institutions, and NBFCs. The goal is to build an internal credit scoring mechanism using applicant information combined with raw bureau data.

Objective

The primary goal of this study is to assist Home Credit in deciding which loan applications should be approved and which should be rejected. This decision will be based on the applicant's past behavior and application details.

Data Description

The model-building data consists of two tables:

1. Applications Table

SK_ID_CURR: Unique identifier for the applications table.

Contains 122 features describing each loan applicant.

TARGET: Dependent variable for classification (1 - client with payment difficulties, 0 - all other cases).

Feature selection is required to drop unhelpful or redundant features before model training.

2. Bureau Table

SK_ID_BUREAU: Unique identifier for the bureau table.

Contains 17 features stored at the trade level.

SK_ID_CURR links to the applications table.

Includes credit behavior of each trade.

Feature engineering is required to aggregate trade-level data at SK_ID_CURR level for integration with the applications table.

Task Breakdown

As a Business Analyst for Home Credit, your responsibilities include:

Data Gathering & Cleaning:

Collect, process, and clean raw data to ensure usability.

Feature Engineering:

Aggregate trade-level data at the applicant level to capture payment behavior.

Create manual features that contribute to the model.

Examples of engineered features:

Number of trades reported in the bureau (count of trades per applicant)

Number of active vs. closed trades (based on CREDIT_ACTIVE)

Max CREDIT_DAY_OVERDUE (maximum value of CREDIT_DAY_OVERDUE)

Most frequent currency (mode of CREDIT_CURRENCY)

Model Development:

Build a classification model to distinguish between approved and rejected applicants.

Key Business Questions

As a Business Analyst, you need to address the following questions:

How can trade-level data from Credit Bureaus be aggregated at the applicant level to capture payment behavior effectively?

Which application or payment behavior factors significantly influence an applicant’s borrowing behavior for newly disbursed loans?

How can these identified factors be leveraged in a predictive model for decision-making?

Once the model is built, how can its outputs be translated into business strategies and insights for the bank?
