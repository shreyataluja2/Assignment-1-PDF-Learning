# Assignment 1

## 📌 Title  
Learning Probability Density Functions using a Roll-Number-Parameterized Non-Linear Model

---

## 📂 Repository Contents
- Assignment-1.pdf  
- Shreya_102313020_3L3.ipynb  
- README.md  

---

## 📖 Introduction
This assignment focuses on learning a Probability Density Function (PDF) from real-world air quality data using a roll-number-parameterized non-linear transformation. The objective is to transform the input data, estimate the parameters of a probability density function, and analyze the learned distribution using numerical results and graphical visualizations.

---

## 📊 Dataset Description
- Dataset: India Air Quality Data  
- Feature Used: NO₂ (Nitrogen Dioxide concentration)  
- Data Type: Continuous numerical data  

The NO₂ feature is selected because it is suitable for probability density estimation.

---

## 🧪 Methodology

### Step 1: Data Preprocessing
- The dataset is loaded and cleaned.
- Missing and invalid NO₂ values are removed.
- The NO₂ column is extracted as the input variable x.

---

### Step 2: Non-Linear Transformation
Each input value x is transformed into z using the roll-number-based transformation:

z = x + aᵣ · arcsin(bᵣ · x)

where:
- aᵣ = 0.05 × (r mod 7)
- bᵣ = 0.3 × ((r mod 5) + 1)
- r is 102313020

This transformation introduces non-linearity and personalizes the data.

---

### Step 3: Probability Density Function Learning
The transformed variable z is modeled using the following PDF:

p̂(z) = c · e^(−λ(z − μ)²)

where:
- μ is the mean
- λ controls the spread
- c is the normalization constant

---

### Step 4: Parameter Estimation
The parameters μ, λ, and c are estimated from the transformed data using statistical methods. These parameters fully define the learned probability density function.

---

## 📋 Results

| Parameter | Description | Value |
|---------|-------------|-------|
| aᵣ | Transformation parameter | 0.25 |
| bᵣ | Transformation parameter | 0.3 |
| μ | Mean of transformed variable z | 22.116537578450416 |
| λ | Spread controlling parameter | 0.002092742404850967 |
| c | Normalization constant | 0.025809699663113164 |


---

## 📈 Result Graphs

### 1. Histogram of Transformed Data (z)
This graph shows the distribution of the transformed values z.

![Histogram of z](histogram_z.png)

---

### 2. Learned Probability Density Function
This graph shows the estimated PDF plotted over the transformed data.

![PDF Curve](pdf_curve.png)

---

### 3. Effect of Non-Linear Transformation
This graph compares original NO₂ values with transformed values.

![Transformation Effect](transformation_effect.png)


---

## 📊 Key Observations
- The roll-number-based transformation personalizes the dataset.
- The transformed data follows a Gaussian-like distribution.
- The learned PDF fits the data effectively.
- Visualizations support the correctness of the model.

---


## ▶️ How to Run
1. Clone the repository  
2. Open `Shreya_102313020_3L3.ipynb`  
3. Run all cells sequentially  

---

## 🎯 Learning Outcomes
- Understanding Probability Density Functions  
- Applying non-linear transformations  
- Estimating PDF parameters  
- Interpreting data using graphs  

---

## 👩‍🎓 Author
Shreya  
Roll Number: 102313020  
Section: 3L3
