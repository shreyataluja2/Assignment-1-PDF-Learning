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

### Step 1: Non-Linear Transformation
The NO₂ values are transformed using a roll-number-based non-linear transformation:

z = x + aᵣ · sin(bᵣ · x)

where:
- aᵣ = 0.05 × (r mod 7)
- bᵣ = 0.3 × ((r mod 5) + 1)
- r is 102313020

This step introduces non-linearity and personalizes the data.

---

### Step 2: Learning the Probability Density Function
The transformed variable z is modeled using the following probability density function:

p̂(z) = c · e^(−λ (z − μ)²)

The parameters μ (mean), λ (spread), and c (normalization constant) are estimated directly from the transformed data.

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
