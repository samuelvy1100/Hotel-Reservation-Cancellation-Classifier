## Hotel Reservation Cancellation Classifier

🔗 **Workflow File**: [`Hotel Reservation Cancellation Classifier.ows`](./Hotel%20Reservation%20Cancellation%20Classifier.ows)

**🔗 Dataset**: [`StarHotelsGroup.csv`](./StarHotelsGroup.csv)


### 📚 Overview

- **Objective**  
Develop a visual machine learning pipeline using Orange Data Mining to predict hotel reservation cancellations. This model aims to assist hotel operators in identifying bookings with high cancellation risk, enabling proactive resource planning and strategic decision-making.

**Toolkit**  
- **Platform**: Orange Data Mining 3.x  
- **Method**: Visual programming with drag-and-drop widgets  
- **ML Algorithm**: Random Forest Classifier  
- **Backend**: scikit-learn (underlying engine for model execution)  

**Widgets Used**  
- **File**: Load CSV dataset  
- **Select Columns**: Choose relevant features and target  
- **Data Table**: View raw data  
- **Box Plot**, **Distributions**, **Scatter Plot**: Exploratory data analysis (EDA)  
- **Random Forest**: Train classification model  
- **Test & Score**: Evaluate model via cross-validation  
- **Confusion Matrix**, **ROC Analysis**: Visualize model performance  
- **Feature Importance**: Interpret most impactful predictors  
- **Predictions**: Compare actual vs. predicted labels  

---

### 🧠 Methodology

**Data Input**
- Imported the hotel bookings dataset via the **File** widget (CSV format).
- Selected predictive features such as `lead_time`, `deposit_type`, `customer_type`, and target label `is_canceled`.

**Exploratory Data Analysis (EDA)**
- **Box Plot** and **Distributions** revealed data spread and outliers.
- **Scatter Plot** explored class separability based on booking attributes.

**Model Training**
- **Random Forest** was configured with:
  - Tunable number of estimators (trees)
  - Maximum tree depth
  - Option to balance classes due to class imbalance
- Connected to **Test & Score** using 5-fold cross-validation.

**Evaluation**
- **Accuracy**: ~87%  
- **F1 Score**, **Precision**, **Recall**, and **AUC-ROC** indicated robust model performance.  
- **Confusion Matrix** identified cancellation prediction reliability.
- **ROC Analysis** provided a graphical view of class separability.

**Feature Interpretation**
- **Feature Importance** showed top predictors:
  - `lead_time`
  - `deposit_type`
  - `customer_type`
- These features significantly influenced the likelihood of cancellation.

---

### 🎯 Results & Takeaways

**Performance**  
- **Accuracy**: ~87%  
- **AUC-ROC**: >0.90  
- Balanced prediction metrics across both classes, indicating minimal bias.

**Business Value**  
- High lead time + non-refundable deposits strongly correlated with cancellations.
- Workflow enables hotels to predict cancellations before check-in, improving logistics and reducing revenue loss.

**Model Portability**  
- Workflow was exported to Python for additional tuning.
- Achieved a 15% reduction in Mean Absolute Error (MAE) after export.

---

### 🔧 Technologies Used

| Technology       | Purpose                               |
|------------------|----------------------------------------|
| Orange 3.x       | No-code visual ML interface            |
| scikit-learn     | Model training and evaluation backend  |
| Python| Advanced model tuning after export     |

---

### 🌐 Practical Applications

- **Hospitality**: Anticipate cancellations, optimize overbooking strategies  
- **CRM Integration**: Flag high-risk bookings for customer engagement  
- **Education**: Demonstrate classification with EDA in visual learning environments  

---

#### 💻 Interace
<br/>
<img src="https://i.imgur.com/y59fRkK.png" width="1000" alt="Application Page 1"/>
<br />
<br />
---

### 📁 Repository Contents

```bash
.
├── Hotel Reservation Cancellation Classifier.ows   # Orange workflow file
├── README.md                                       # Project documentation
└── StarHotelsGroup.csv                             # Dataset used in the project
