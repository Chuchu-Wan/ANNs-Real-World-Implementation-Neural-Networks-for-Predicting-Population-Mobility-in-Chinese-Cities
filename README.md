# ANNs Real-World-Implementation Neural-Networks-for-Predicting-Population-Mobility-in-Chinese-Cities
ANNs Real-World Implementation: Neural Networks for Predicting Population Mobility in Chinese Cities
# The Attractiveness of China Cities: LSTM and FNN for Predicting Population Mobility

## 📌 Overview  

This project explores **population mobility trends** across **633 Chinese cities** over a **13-year period (2010–2022)**. Using advanced machine learning techniques—**Feedforward Neural Networks (FNN)** and **Long Short-Term Memory (LSTM) models**—this study aims to:  

1. **Predict population movement** based on key urban characteristics.  
2. **Identify factors influencing city attractiveness**, such as economic growth, employment, infrastructure, and air quality.  
3. **Provide policy recommendations** to help local governments manage migration challenges and enhance urban development.  

The study is particularly relevant given that **40% of Chinese cities are experiencing population decline**, posing significant policy and economic challenges.  

---

## 📂 Files and Directories  

### **1. Research Paper**  
📄 **[`Wan_Stage5_Paper.pdf`](./Wan_Stage5_Paper.pdf)**  
- The full research paper detailing **research questions, dataset description, methodology, model performance, and policy recommendations**.  
- Key topics include:  
  - Urban-rural migration patterns  
  - Factors influencing city attractiveness  
  - Machine learning techniques for population mobility prediction  

---

### **2. Presentation Slides**  
📊 **[`Wan_Stage5_Slides.pdf`](./Wan_Stage5_Slides.pdf)**  
- A **summary of key findings**, including:  
  - Why some cities attract more residents while others lose population  
  - Model design (FNN vs. LSTM)  
  - Insights for policymakers  

---

### **3. Machine Learning Models**  
🧠 **[`Final_Project_FNN.ipynb`](./Final_Project_FNN.ipynb)**  
- Implementation of a **Feedforward Neural Network (FNN)** model to predict population mobility using structured data.  

⏳ **[`Wan_Stage5_Timesheries.html`](./Wan_Stage5_Timesheries.html)**  
- Implementation of a **Time Series model**, including **LSTM**, to analyze temporal trends in migration patterns.  

---

### **4. Dataset**  
📂 **[`Wan_stage5.csv`](./Wan_stage5.csv)**  
- Contains **195 urban features** for **633 Chinese cities (2010–2022)**.  
- Key features include:  
  - **GDP Growth**: Measures economic vitality and job creation.  
  - **Housing Prices**: Reflects economic prosperity and affordability challenges.  
  - **Employment Structure**: Share of jobs in primary, secondary, and tertiary sectors.  
  - **Air Quality (PM2.5 levels)**: Key determinant of urban livability.  
  - **Education Resources**: Number of university students per capita.  
  - **Healthcare Access**: Hospital beds and number of doctors per capita.  
  - **Public Transport Infrastructure**: Road mileage and public transit coverage.  

---

## 🏗 Methodology  

### **1. Dataset Preprocessing**  
- Data is sourced from the **China Urban Database** covering 13 years.  
- **Missing data handling**:  
  - Housing prices (~15% missing)  
  - Public library collections (~12% missing)  
  - **KNN imputation** used for filling gaps.  

### **2. Machine Learning Models**  

#### **🔹 Feedforward Neural Network (FNN)**
- Efficient for structured, non-sequential data.  
- Captures **non-linear relationships** between urban features and population movement.  
- **Faster computation** compared to LSTM.  
- Architecture:  
  - **Input Layer**: Dense(128) with ReLU activation.  
  - **Hidden Layers**:  
    - Dense(64) → Dropout(0.2)  
    - Dense(32)  
  - **Output Layer**: Dense(1)  
- **Training Parameters**:  
  - 50 epochs  
  - Batch size = 32  

#### **🔹 Long Short-Term Memory (LSTM)**
- Designed for **time-dependent** migration patterns.  
- Retains **temporal dependencies** using **memory cells**.  
- More suitable for **long-term forecasting** than FNN.  
- Architecture:  
  - **Input Layer**: LSTM (64 units, L2 regularization).  
  - **Hidden Layers**: Dense(32) → Dropout(0.5).  
  - **Output Layer**: Dense(1).  
- **Early Stopping**: Stops training if validation loss does not improve for 10 epochs.  

---

## 📊 Model Performance  

| Model  | Test MSE  | Test MAE  |
|--------|----------|----------|
| **FNN**  | **0.01115** | **0.065375** |
| **LSTM** | 0.0391  | 0.10365  |

- **FNN performs better** in terms of Mean Squared Error (MSE) and Mean Absolute Error (MAE), making it more efficient for structured data.  
- **LSTM captures temporal dependencies** but is computationally more expensive.  

---

## 🔎 Key Findings  

### **1. Factors Driving Migration**  
- **Urban-Rural Gap**: Rural residents move to cities for better jobs and infrastructure.  
- **Talent Gap**: Small cities struggle to retain young professionals.  
- **Urban Competitiveness**: Cities with better economic conditions, infrastructure, and public services attract more residents.  

### **2. Policy Recommendations**  
- **For Outflowing Cities**:  
  - **Create economic incentives** to retain talent.  
  - **Improve public services** (healthcare, education, transportation).  
  - **Boost local job markets** to reduce reliance on megacities.  

- **For Inflowing Cities**:  
  - **Manage urban growth** to prevent overpopulation issues.  
  - **Enhance housing affordability** to accommodate migrants.  
  - **Invest in public infrastructure** to sustain quality of life.  

---

## 📌 Future Work  

🔸 **Improve data quality**  
- Expand dataset with **real-time migration data** from government portals.  
- Implement **advanced imputation techniques** for missing values.  

🔸 **Enhance model performance**  
- Experiment with **ensemble models** (combining FNN & LSTM).  
- Fine-tune hyperparameters for better generalization.  

🔸 **Policy impact assessment**  
- Test **alternative urban planning strategies** using model predictions.  
- Evaluate **long-term implications** of migration trends.  

---

## 👩‍💻 Author  

👤 **Chuchu Wan**  
🎓 **MPP | McCourt School of Public Policy, Georgetown University (Class of 2024)**  
📍 Research Interests: Urban Economics, Migration, Data Science for Public Policy  

---

## 📢 Citation  

If you use this research or dataset, please cite:  

> Wan, Chuchu. *The Attractiveness of China Cities: LSTM and FNN for Predicting Population Mobility*. McCourt School of Public Policy, Georgetown University, 2024.  

---

## 🎯 Acknowledgments  

This project was conducted as part of **PPOL 6821 - Applied Neural Networks** at the **McCourt School of Public Policy**. Special thanks to **faculty advisors and peers** for their valuable feedback.  

---

## 📬 Contact  

📧 Email: [cw1215@georgetown.edu](mailto:cw1215@georgetown.edu)  
🔗 LinkedIn: [linkedin.com/in/chuchuwan](https://www.linkedin.com/in/chuchu-wan-653171289)  

---
