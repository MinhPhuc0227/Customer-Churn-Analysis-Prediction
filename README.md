> **English version below.**
# Customer Churn Analysis & Prediction

## Giới thiệu

Dự án thực hiện phân tích hành vi khách hàng và xây dựng mô hình Machine Learning
để dự đoán khả năng khách hàng rời bỏ dịch vụ (Customer Churn) bằng bộ dữ liệu
Telco Customer Churn.

Mục tiêu của dự án là xác định các yếu tố chính liên quan đến việc khách hàng
rời bỏ và đưa ra các insight kinh doanh nhằm hỗ trợ xây dựng chiến lược giữ chân
khách hàng.

## Mục tiêu

- Phân tích đặc điểm khách hàng và xu hướng rời bỏ dịch vụ
- Xác định các yếu tố chính liên quan đến Customer Churn
- So sánh và đánh giá các mô hình Machine Learning khác nhau
- Lựa chọn mô hình phù hợp để dự đoán Customer Churn
- Chuyển đổi kết quả phân tích thành các đề xuất hỗ trợ giữ chân khách hàng

## Dataset

Bộ dữ liệu gồm **7.043 bản ghi khách hàng** với **21 thuộc tính**, bao gồm thông
tin khách hàng, dịch vụ sử dụng, thông tin tài khoản, thanh toán và trạng thái
rời bỏ dịch vụ.

**Nguồn:** [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## Quy trình phân tích

### 1. Chuẩn bị dữ liệu
- Làm sạch và tiền xử lý dữ liệu
- Xử lý các giá trị thiếu và không nhất quán
- Biến đổi và mã hóa đặc trưng
- Chuẩn hóa dữ liệu

### 2. Phân tích khám phá dữ liệu (EDA)
- Phân tích đặc điểm khách hàng và xu hướng Customer Churn
- Trực quan hóa mối quan hệ giữa các thuộc tính và khả năng rời bỏ
- Xác định các yếu tố tiềm năng liên quan đến Customer Churn

### 3. Feature Engineering
- Mã hóa các biến phân loại
- Chuẩn hóa các biến số
- Chuẩn bị dữ liệu đầu vào cho các mô hình Machine Learning

### 4. Xây dựng & đánh giá mô hình

Đánh giá **9 mô hình Machine Learning** bằng phương pháp **5-fold Cross-Validation**:

- Logistic Regression
- Decision Tree
- Random Forest
- AdaBoost
- Gradient Boosting
- XGBoost
- LightGBM
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

Các mô hình được đánh giá bằng các chỉ số Accuracy, F1-Score, Confusion Matrix
và ROC-AUC.

## Kết quả

**Logistic Regression** được lựa chọn là mô hình tối ưu với độ chính xác trung
bình khoảng **80%**.

Mô hình đạt **F1-Score = 0.598** đối với lớp Churn.

### Các yếu tố chính ảnh hưởng đến Customer Churn

Phân tích xác định một số yếu tố quan trọng liên quan đến khả năng khách hàng
rời bỏ:

- Loại hợp đồng
- Thời gian sử dụng dịch vụ (Tenure)
- Phí dịch vụ hàng tháng (Monthly Charges)

Các yếu tố này có thể được sử dụng để xác định nhóm khách hàng có nguy cơ
rời bỏ cao hơn.

## Business Insights

Dựa trên kết quả phân tích, doanh nghiệp có thể tập trung vào các khách hàng
có nguy cơ rời bỏ cao bằng cách xem xét các yếu tố như loại hợp đồng, thời gian
sử dụng dịch vụ và phí hàng tháng.

Các kết quả này có thể hỗ trợ doanh nghiệp xác định khách hàng có nguy cơ rời
bỏ và xây dựng các chiến lược giữ chân phù hợp.

## Công nghệ sử dụng

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## Hướng dẫn chạy trên Google Colab

1. **Tải dataset** từ [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).
2. Mở file `Customer_Churn_Analysis.ipynb` bằng Google Colab.
3. Upload file dataset `WA_Fn-UseC_-Telco-Customer-Churn.csv` vào môi trường Google Colab.
4. Chạy lần lượt các cell từ trên xuống dưới.

### Đọc dataset

Notebook đọc dataset trực tiếp từ file CSV đã upload vào Google Colab:

```python
dataset = pd.read_csv("/WA_Fn-UseC_-Telco-Customer-Churn.csv") 
```

---

# English Version

## Overview

This project analyzes customer behavior and develops a machine learning model to predict customer churn using the Telco Customer Churn dataset.

The project aims to identify key factors associated with customer churn and provide business insights that can support customer retention planning.

## Objectives

- Analyze customer characteristics and churn patterns
- Identify key factors associated with customer churn
- Compare and evaluate different machine learning models
- Select an appropriate model for churn prediction
- Translate analytical findings into customer retention recommendations

## Dataset

The dataset contains **7,043 customer records** with **21 attributes** covering customer information, subscribed services, account details, payment information, and churn status.

**Source:** [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)

## Analysis Process

### 1. Data Preparation
- Data cleaning and preprocessing
- Handling missing and inconsistent values
- Feature transformation and encoding
- Feature scaling

### 2. Exploratory Data Analysis
- Analyzed customer characteristics and churn patterns
- Visualized relationships between customer attributes and churn
- Identified potential factors associated with customer churn

### 3. Feature Engineering
- Encoded categorical variables
- Standardized numerical features
- Prepared features for machine learning models

### 4. Model Development & Evaluation

Evaluated **9 machine learning models** using **5-fold cross-validation**:

- Logistic Regression
- Decision Tree
- Random Forest
- AdaBoost
- Gradient Boosting
- XGBoost
- LightGBM
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

Models were evaluated using classification performance metrics, including Accuracy, F1-Score, Confusion Matrix, and ROC-AUC.

## Results

**Logistic Regression** was selected as the optimal model, achieving approximately **80% average accuracy**.

The model also achieved an **F1-Score of 0.598 for the Churn class**.

### Key Churn Factors

The analysis identified several important factors associated with customer churn:

- Contract type
- Customer tenure
- Monthly charges

These findings provide a basis for identifying customers with a higher risk of churn.

## Business Insights

Based on the analysis, customer retention strategies can focus on customers with higher churn risk by considering factors such as contract type, tenure, and monthly charges.

The findings can support businesses in identifying at-risk customers and developing targeted retention strategies.

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook / Google Colab

## How to Run in Google Colab

1. **Download the dataset** from [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).
2. Open `Customer_Churn_Analysis.ipynb` in Google Colab.
3. Upload the downloaded dataset file `WA_Fn-UseC_-Telco-Customer-Churn.csv` to the Colab environment.
4. Run the notebook cells sequentially from top to bottom.

### Dataset Loading

The notebook loads the dataset directly from the uploaded CSV file:

```python
dataset = pd.read_csv("/WA_Fn-UseC_-Telco-Customer-Churn.csv")
