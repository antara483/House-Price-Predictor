# Housing Price Predictor 🏠💰

Ever wondered how much a house is really worth? This project is my attempt to **predict house prices** using machine learning, based on features like area, number of bedrooms/bathrooms, stories, amenities, and furnishing status. Along the way, I explored the data, engineered new features, and built a **Multiple Linear Regression model** to estimate prices with decent accuracy.  

Here’s how the Actual Vs Predicted Prices looks:

![Confusion Matrix](images/Screenshot%201.png)

Here’s the Residuals Vs Predicted Values:

![Accuracy Score](images/Screenshot%202.png)

And the QQ Plot of Residuals:

![Accuracy Score](images/Screenshot%203.png)

---
Dataset[https://www.kaggle.com/datasets/harishkumardatalab/housing-price-prediction]

## Technology Used 🛠️

- Python 3.x – Core programming language

- Pandas – Data manipulation and analysis

- NumPy – Numerical computing

- Scikit-learn – Machine learning modeling, preprocessing, and evaluation

- Matplotlib & Seaborn – Data visualization

- SciPy – Statistical analysis


  
## What I Did ✨

### Data Exploration & Cleaning
- Took a good look at the dataset — checked for missing values, duplicates, and column info.  
- Explored categorical features like `furnishingstatus` and `mainroad` to understand the patterns.  

### Encoding Categorical Variables
- Used `LabelEncoder` to convert binary features into numbers.  
- Applied `One-Hot Encoding` for `furnishingstatus` to make it model-friendly.  

### Feature Engineering
- Combined bedrooms and bathrooms into a single `total_rooms` feature.  
- Calculated `area_per_room` to see space efficiency.  
- Created `stories_area` as area × stories — because bigger and taller houses matter!  
- Combined `guestroom` and `basement` into `has_guest_basement`.  
- Counted the number of amenities (`airconditioning`, `hotwaterheating`, `prefarea`, `mainroad`) into `amenities_count` to quantify comfort.  

### Data Preprocessing
- Split the dataset into training (80%) and testing (20%).  
- Scaled the `area` feature using `StandardScaler` for better model performance.  

### Modeling
- Trained a **Multiple Linear Regression model** on the processed data.  
- Evaluated it using **MAE, MSE, and R² score** to see how well it predicts.  

### Visualization
- Heatmap to check feature correlations.  
- Scatter plot comparing **Actual vs Predicted Prices**.  
- Residual plot to see where the model over- or under-predicts.  
- QQ plot to check if residuals are normally distributed.  

---

## Insights 🔍
- `area`, `total_rooms`, and `amenities_count` are strong influencers of house price.  
- Residuals are mostly centered around zero — nice fit!  
- This model gives a reasonable estimate of house prices, and can be extended with more features or complex models for better accuracy.  


