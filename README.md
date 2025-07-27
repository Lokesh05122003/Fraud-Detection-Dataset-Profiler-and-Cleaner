# 🛡️ Fraud Detection Dataset Profiler and Cleaner

An end-to-end **automated data preprocessing pipeline** designed to accelerate fraud detection model development using AWS services. This project profiles, cleans, and transforms raw datasets into model-ready formats, generating detailed reports and ensuring reproducibility via infrastructure-as-code.

[🔗 Resume Project Link](https://github.com/Lokesh05122003/Fraud-Detection-Dataset-Profiler-and-Cleaner/tree/main?tab=readme-ov-file#%EF%B8%8F-setup-instructions)

---

## 📌 Overview

This solution automates the process of:

- Profiling fraud detection datasets
- Cleaning and transforming input CSV data
- Generating data quality reports
- Delivering cleaned data for ML training
- Deploying infrastructure using AWS CloudFormation

It is based on the [AWS blog](https://aws.amazon.com/blogs/machine-learning/automate-data-profiling-and-cleaning-for-fraud-detector-datasets/) by **Hao Zhou** and **Anqi Cheng**, tailored for real-world enterprise use cases.

---

## 🏗️ Architecture

The project follows a fully serverless architecture using the following AWS services:

- **Amazon S3**: Stores raw input data, profiling reports, and cleaned CSVs
- **AWS Lambda**: Triggers the workflow and orchestrates AWS Glue jobs
- **AWS Glue**: Handles data profiling, transformation, and export
- **AWS CloudFormation**: Automates the deployment of all components

📊 Outputs:
- **HTML profiling reports**
- **Cleaned, transformed CSVs**

![Architecture Diagram](./images/architecture.png)

---

## ✨ Key Features

- 📋 **Data Profiling**: Automated analysis using AWS Glue to assess column types, nulls, uniqueness, etc.
- 🧹 **Data Cleaning**: Removes duplicates, handles missing values, and converts types
- 📁 **Exported Artifacts**:
  - `report.html`: Profiling summary
  - `cleaned_data.csv`: Final dataset for ML
- ☁️ **CloudFormation Integration**: One-click stack deployment for fast onboarding
- 🔁 **Fully Reproducible**: Designed for repeated experimentation and versioned datasets

---

## 🚀 Technologies Used

| Service         | Purpose                              |
|-----------------|--------------------------------------|
| AWS Lambda      | Trigger Glue jobs and handle logic   |
| AWS Glue        | Profile and clean raw CSV datasets   |
| Amazon S3       | Data storage and reporting output    |
| CloudFormation  | Infra as Code for easy setup         |

---

## 🧰 Setup Instructions

### Prerequisites
- AWS Account with permission to use Lambda, Glue, S3, CloudFormation
- Python 3.8+ and AWS CLI configured
- IAM Role for Glue and Lambda

### 🚨 Steps

1. **Clone the Repository**

```bash
git clone https://github.com/Lokesh05122003/Fraud-Detection-Dataset-Profiler-and-Cleaner.git
cd Fraud-Detection-Dataset-Profiler-and-Cleaner
