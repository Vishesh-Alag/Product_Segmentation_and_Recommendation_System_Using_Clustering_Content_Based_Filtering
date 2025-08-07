

# 🛍️ Product Segmentation and Recommendation System Using Clustering & Content Based Filtering

A robust end-to-end machine learning (unsupervised learning *Clustering* ) project for **product segmentation and personalized recommendations** using large-scale retail transaction data (~3 lakh rows across 30 features). This project combines **EDA**, **clustering**, **statistical analysis**, and **content-based filtering** to deliver actionable business insights and intelligent product suggestions.

---

## 📌 Project Overview

This project solves key business challenges in the e-commerce space:

- 🔍 Identify meaningful product clusters via unsupervised learning
- 🧠 Predicting product segments in real-time from user input
- 🎯 Recommend similar products using content-based filtering
- 📊 Empower business intelligence with statistical and visual insights

---

## 💡 Problem Statement

E-commerce businesses often struggle with:
- Managing diverse product portfolios
- Optimizing inventory based on product performance
- Providing personalized recommendations
- Segmenting products for targeted marketing
- Extracting meaningful insights from raw transaction data

---

## 🎯 Objectives

### Primary
- ✅ Segment products into distinct clusters using machine learning
- ✅ Build a real-time, content-based recommendation system
- ✅ Enable product cluster prediction from user input
- ✅ Extract statistical insights for strategic decisions

### Secondary
- ✅ Implement a reusable data preprocessing pipeline
- ✅ Conduct comprehensive exploratory data analysis (EDA)
- ✅ Visualize patterns in sales, reviews, customer types, and geography

---

## 🧠 Techniques & Approaches

### 🔄 Data Preprocessing
- Duplicates & Missing Values Handling
- Feature Engineering (e.g., Feedback to Score)
- Categorical Encoding (OneHotEncoder)
- Scaling (StandardScaler)
- Outlier Detection using IQR

### 📊 Exploratory Data Analysis (EDA)
- Histograms, Boxplots, Pairplots, Countplots
- Correlation Heatmaps
- Categorical Distribution Visuals
- Temporal Analysis: Monthly, Yearly, Hourly trends
- Geo Analysis: Top Cities, States, Countries

### 📈 Unsupervised Learning
- Algorithm: `MiniBatchKMeans` Clustering (k=4)
- Features Used:
  - Categorical: `Product_Category`, `Product_Brand`, `Product_Type`
  - Numerical: `Total_Amount`, `Ratings`, `Feedback_Score`
- Validation:
  - Elbow Method & Silhouette Score
  - PCA Visualization (2D) → 51.8% explained variance

**Cluster Interpretations:**
1. 📚 Customer Favorites: Books & Electronics with high ratings  
2. 💰 High Revenue Essentials: Premium electronics  
3. 🛒 Mass Grocery Products: High volume, moderate quality  
4. 📉 Low Performing Generics: Poor ratings, low spend

### 🎛️ Real-Time Product Cluster Prediction
- Users can input product attributes and receive the predicted cluster label instantly.
- Powered by the saved clustering model and preprocessing pipeline (`pickle` files).

### 🔁 Recommendation System
- Type: Content-Based Filtering using Cosine Similarity
- Inputs:
  - One-hot encoded categorical + scaled numerical features
- Features:
  - Customizable filters: Min. rating, same brand/type/category
  - No dependency on user behavior (cold-start safe)

### 📐 Statistical Testing
- ✅ Chi-Square: Product Category vs Customer Segment → Significant
- ✅ Kruskal-Wallis: Spending across categories → No significant difference
- ✅ Mann-Whitney: Male vs Female spending → No difference
- ✅ Chi-Square: Payment vs Customer Segment → Highly significant

---

## 🧪 Dataset Overview

- 📦 Rows: `293,908`
- 📌 Columns: `30`
- 🗂️ Source: `new_retail_data.csv` (User Upload)

| Feature Type       | Columns |
|--------------------|---------|
| Categorical        | Product Category, Brand, Type, Gender, Feedback, etc. |
| Numerical          | Age, Amount, Ratings, Total_Purchases, etc. |
| Temporal           | Date, Month, Year, Time |
| Geo                | Country, State, City |

---

## 📊 Key EDA Insights

- 📈 Age: Bimodal (Young adults & middle-aged dominate)
- 💵 Spending: Uniform across income levels & payment methods
- 🛍️ Feedback: Matches rating perfectly (Bad → 1, Excellent → 4)
- 🚚 Shipping: 69% prefer premium (Same-day or Express)
- 💳 Digital Payments: 75% adoption
- 📦 Product Mix: Electronics & Grocery are top-performing categories
- 🌎 Top Markets: USA, UK, Germany; Cities like Chicago & Portsmouth

---

## 📦 Deliverables

- ✅ Cleaned & Processed Dataset
- ✅ Clustering Labels with PCA Visualization
- ✅ Trained & Pickled ML Models
- ✅ Interactive Cluster Prediction System
- ✅ Customizable Recommendation Engine
- ✅ Visual Dashboards (Histograms, Heatmaps, Trends)
- ✅ Statistical Reports with Business Insights

---

## 🛠️ Tech Stack

| Tool            | Purpose |
|-----------------|---------|
| Python          | Core Programming |
| Pandas, NumPy   | Data Wrangling |
| Seaborn, Matplotlib | Visualization |
| Scikit-learn    | Clustering, Scaling, Encoding |
| SciPy           | Statistical Testing |
| Pickle          | Model Serialization |
| Google Colab     | Notebook execution |

---

## 🚀 How to Run This Project

1. Open the [Google Colab Notebook](#) *(Link to your notebook if public)*
2. Upload the dataset file: `new_retail_data.csv`
3. Click on `Runtime > Run all`
4. The following will run automatically:
   - Data Cleaning
   - Clustering
   - Recommendation Engine
   - Visualization
5. **Try real-time features:**
   - 🧩 Predict which cluster a new product belongs to by entering its details
   - 🤖 Get similar product recommendations using your chosen filters


---

## 📈 Business Value

This project enables:
- 🎯 Targeted marketing using product segments
- 🛒 Better inventory planning using sales patterns
- 💬 Personalized user experience via recommendations
- 📊 Real-time insights for product and revenue strategy



---

