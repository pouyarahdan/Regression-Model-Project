# 🚗 Car Price Prediction using Linear Regression

This project builds a regression model to predict the selling price of used cars based on features like age, current price, kilometers driven, fuel type, seller type, transmission type, and ownership history.

---

## 📦 Dataset

The dataset includes the following columns:

- Year: Year of manufacture
- Present_Price: Price at the time of selling
- Kms_Driven: Distance driven
- Fuel_Type: Petrol / Diesel / CNG
- Seller_Type: Dealer / Individual
- Transmission: Manual / Automatic
- Owner: Number of previous owners
- Selling_Price: Target variable

---

## 📈 Workflow

### 🧹 1. Data Cleaning & Preprocessing
- Removed irrelevant columns like Car_Name
- Created new feature: Age_Car = 2024 - Year
- Converted categorical features to numerical values
- Replaced string labels with numeric codes

### 📊 2. Exploratory Data Analysis (EDA)
- Scatter plots of all features vs. Selling_Price
- Histograms for numerical columns
- Bar plots for categorical distributions

### 🧠 3. Model Training
- Linear Regression using train_test_split with multiple test sizes
- Evaluation metrics used:
  - MAE (Mean Absolute Error)
  - MSE (Mean Squared Error)
  - RMSE (Root Mean Squared Error)
  - R² Score

### 🔍 4. Feature Engineering
- Applied power transformation on features (powers 1 to 9)
- Found the best transformation (e.g., Owner^9)
- Re-trained model with transformed features

### 🔁 5. Cross-Validation
- Performed K-Fold (5 splits) cross-validation to ensure stability

### 🔎 6. Manual Prediction
- Used final model coefficients to predict price of a car with custom input manually

---

## 📊 Results

| Metric        | Before Tuning | After Tuning |
|---------------|---------------|--------------|
| MAE           | 1.100         | 0.861        |
| MSE           | 2.784         | 1.427        |
| RMSE          | 1.695         | 1.194        |
| R² Score      | 0.822         | 0.946 ✅ |

📌 The final model showed improved performance and generalization after removing outliers and applying transformations.

---

## 📂 Project Structure
Regression-Model-Project/ ├── Data/cardata.csv ├── Linear-Regression-Project.ipynb ├── README.md ├── LICENSE ├── .gitignore

---

## 🛠️ Technologies Used

- Python 3.x
- Jupyter Notebook
- pandas, numpy
- matplotlib
- scikit-learn

---

## 📌 Usage Example

To predict a new car's price:

`python
# Sample Inputs
age = 10
present_price = 11.23
kms_driven = 42000
fuel_type = 2         # Petrol
seller_type = 1       # Dealer
transmission = 0      # Manual
owner = 1

# Model Equation
selling_price = intercept + (c1 * age) + (c2 * present_price) + ...


---

📬 Contact

Developed with 💻 and ☕ by Pouya Rahdan
📧 pouya.rahdan5@gmail.com
🔗 GitHub: github.com/pouyarahdan


---

📄 License

MIT License. See LICENSE for details.
