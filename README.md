# Customer Segmentation for Brazilian Online Retail

## Overview

This project focuses on segmenting customers of an online retail platform using machine learning techniques.

The goal is to move from generic marketing strategies to **data-driven, targeted customer engagement**, by identifying distinct customer groups based on behaviour, spending patterns, and satisfaction levels.

This project was completed as part of the BITS Pilani MSc Artificial Intelligence and Data Science programme.

---

## Problem Statement

Retail businesses deal with diverse customer behaviour, making it inefficient to use a single marketing strategy for all users.

Without segmentation:
- marketing spend is wasted
- engagement is low
- customer retention suffers

This project solves that by identifying **distinct customer segments** using real-world e-commerce data.

---

## Business Goal

The objective is to build a segmentation model that helps:

- identify high-value customers
- detect low-satisfaction users
- understand purchasing behaviour
- support targeted marketing campaigns
- improve retention and repeat purchases

---

## Dataset

This project uses the **Brazilian E-Commerce Public Dataset (Olist)** from Kaggle.

It contains:
- ~100,000 orders
- customer profiles
- payment details
- product data
- seller information
- customer reviews

Dataset link:

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

---

## Tools and Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Google Colab

---

## Project Workflow

### 1. Data Collection
- Downloaded dataset using Kaggle API
- Loaded multiple tables

### 2. Data Cleaning
- handled missing values
- removed duplicates
- corrected formats

### 3. Data Merging
- merged orders, customers, payments, reviews, products

### 4. Feature Engineering
Created customer-level features:
- Recency
- Frequency
- Monetary value
- Average order value
- Review score
- Delivery performance
- Payment behaviour

### 5. Feature Transformation
- scaling
- encoding
- PCA for dimensionality reduction

### 6. Model Building
- K-Means clustering
- Gaussian Mixture Model comparison

### 7. Evaluation
- Silhouette Score
- Davies-Bouldin Index
- cluster size distribution

---

## Key Results

The model segmented ~96,000 customers into **11 distinct groups**.

Key segments identified:

### High-Value Customers
- high spend
- potential for retention strategies

### Dissatisfied Customers
- low review scores
- need service improvement

### Basket Builders
- higher items per order
- ideal for bundling strategies

### Standard Customers
- average behaviour
- suitable for loyalty programs

---

## Business Recommendations

- target high-value users with retention offers
- re-engage dormant customers
- investigate dissatisfaction drivers
- design personalized campaigns per segment
- track movement between segments over time

---

## Why This Project Matters

This project shows how machine learning can be used to solve **real business problems**, not just build models.

It demonstrates:
- end-to-end ML workflow
- business interpretation of data
- translating insights into actionable strategy

---

## Repository Structure
customer-segmentation-brazilian-ecommerce/

├── README.md
├── src/
│ └── customer_segmentation_pipeline.py
├── docs/
│ └── project_details.pdf
├── presentation/
│ └── customer_segmentation_presentation.pdf


---

## How to Run

Clone the repository:
git clone https://github.com/chetanpant/customer-segmentation-brazilian-ecommerce.git


Install required libraries:
pip install pandas numpy matplotlib seaborn scikit-learn


Run the script:
python src/customer_segmentation_pipeline.py


---

## Project Context

This project was developed as part of the Advanced Apex Project at BITS Pilani.

It integrates data processing, feature engineering, machine learning, and business interpretation into a single workflow.

---

## What This Project Demonstrates

- end-to-end machine learning workflow
- customer segmentation using clustering
- feature engineering from real-world data
- business interpretation of model outputs
- translating insights into strategy
