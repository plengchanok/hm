# H&M Personalized Fashion Recommendation

## Project Overview
This project builds a **Personalized Fashion Recommendation System** using the **H&M Personalized Fashion Recommendations dataset**.  
The goal is to perform customer segmentation using Recency Frequency Monetary (RFM) Model and K-Means clustering to predict and recommend **relevant products** to customers based on their past interactions.

## Dataset Information
The dataset is sourced from [Kaggle's H&M Personalized Fashion Recommendations](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/).  
It consists of three main tables:

### 1️⃣ **Transactions (`transactions_train.csv`)**
- Contains historical purchase data of customers.
- **Columns:**
  - `t_dat` → Transaction date
  - `customer_id` → Unique customer identifier
  - `article_id` → Product ID
  - `price` → Price of the product at purchase
  - `sales_channel_id` → 1 = Online, 2 = Store purchase

### 2️⃣ **Articles (`articles.csv`)**
- Contains metadata about the fashion items.
- **Columns:**
  - `article_id` → Unique product ID
  - `product_code` → Product category code
  - `product_type_no` → Product type number
  - `graphical_appearance_no` → Image style
  - `perceived_colour_value_id` → Light/Dark color category
  - `perceived_colour_master_id` → Main color (e.g., red, blue)
  - `department_no` → Department category
  - `detail_desc` → Detailed product description

### 3️⃣ **Customers (`customers.csv`)**
- Contains information about each customer.
- **Columns:**
  - `customer_id` → Unique customer identifier
  - `FN` → Loyalty program membership flag
  - `Active` → Active status in loyalty program
  - `club_member_status` → Membership type
  - `fashion_news_frequency` → Email subscription frequency
  - `age` → Customer's age

## **Project Workflow**
1. **Exploratory Data Analysis (EDA)**:
   - Purchase trends over time
   - Bestselling products
   - RFM and K-Means Clustering for customer segmentation
2. **Building Recommendation Models**:
   - Use co-occurence to find most frequently purchase together products
3. **Deploying the Model**:
   - Recommend Iems Frequently Purchased Together
   - Generating top 12 fashion recommendations per customer
   - Fill the rest with popular items
