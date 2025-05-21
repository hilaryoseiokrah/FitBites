# 🍽️ FitBites: Your Personalized Ghanaian Meal Recommendations System for Weight Management

**By Hilary Osei-Okrah**  
BSc Computer Science, Ashesi University

---

## 🧠 Overview

**FitBites** is an AI-powered nutrition recommendation system tailored for Ghanaian users who want to manage their weight through culturally relevant food plans. It moves beyond generic fitness apps by offering **affordable, locally sourced meal suggestions**, using cutting-edge machine learning models trained on real nutritional data from Ghanaian cuisine.

This project explores two core models for food recommendation:

- **Autoencoder-based Neural Network (ANN)** 
- **K-Nearest Neighbors (KNN)** 
---

## 🔍 Problem Statement

Most global fitness apps are culturally misaligned, recommending foreign meals that are expensive and inaccessible to the average Ghanaian. This makes consistent weight management difficult, especially for users who need **realistic local alternatives**.

FitBites addresses this by:
- Building a **nutritional embedding space** from Ghanaian food data
- Recommending **meals with similar macronutrient profiles**
- Generating portion-controlled 7-day meal plans based on the user’s weight goal and Total Daily Energy Expenditure (TDEE)

---

## 📁 Project Structure

| File | Description |
|------|-------------|
| `gh_food_nutritional_values.csv` | Dataset of Ghanaian foods with nutritional info |
| `Autoencoder_Model_Thesis.ipynb` | Trains an autoencoder to learn compressed nutrition embeddings and recommends similar meals |
| `KNN_Model_Thesis.ipynb` | Implements KNN  for food recommendation |
| `README.md` | Project overview and documentation |

---

## 🔬 Methodology

### 1. **Data Preprocessing**
- Normalized food nutrient values (`Protein`, `Fat`, `Carbs`, etc.)
- Filled null values

### 2. **Model 1: Autoencoder (ANN)**
- Learns a 16-dimensional embedding of foods
- Recommends similar meals based on cosine similarity of embeddings
- Evaluated using:
  - Top-5 Cosine Similarity (avg ≈ 0.94)
  - User relevance scores (82.5% very relevant)

### 3. **Model 2: KNN from Scratch**
- Computes cosine similarity manually
- Builds a KNN recommendation engine without scikit-learn
- Visualizes clusters and food neighborhoods using PCA + KMeans
- Evaluated using:
  - Top-5 Cosine Similarity (avg ≈ 0.88)
  - F1-score  ≈ 0.83 

---

## 🎯 Features

- ✅ Personalized recommendations based on user's preferred Ghanaian foods
- ✅ BMI and TDEE calculation for caloric goal setting
- ✅ 7-day meal plan generator with portion estimates
- ✅ Partial reshuffling and recipe generation
- ✅ User-tested for relevance and accessibility

---

## 📈 Visualizations

- **t-SNE and PCA plots** showing food clusters
- Color-coded neighborhoods for intuitive understanding of food proximity
- 
- KNN neighborhood maps for selected meals

<p align="center">
  <img src="https://github.com/yourusername/FitBites/blob/main/path-to-visualization.png" width="600"/>
</p>

---

## 🧪 Evaluation Metrics

| Model | Evaluation Metric | Score |
|-------|-------------------|-------|
| Autoencoder | Avg. Top-5 Cosine Similarity | 0.94 |
| Autoencoder | Avg. User Rating | 4.4 / 5 |
| KNN | Avg. Top-5 Cosine Similarity| 0.88 |
| KNN | Avg. User Rating | 3.5 / 5  |

---

## 🧭 Future Work

- ✅ Add dynamic user feedback into the system.
- 🔄 Explore hybrid models to see if there is improvement in the system.
- 🌍 Expand dataset to include foods from all regions in Ghana 
- 📱 Deploy as a full mobile application with offline support

---
## Conclusion
- The autoencoder-based ANN model performed better and was highly preferred by users.
- This is the model that was used in the final application.

---

## 🙏 Acknowledgements

Thanks to the Ashesi University Computer Science Department for supporting this thesis and to all the testers who contributed to the usability validation.

---

## 🛠️ Technologies Used

- Python, PyTorch
- scikit-learn
- Pandas, NumPy, Matplotlib, Seaborn
- Streamlit (for web app deployment)

---

## 📬 Contact

Feel free to reach out for collaboration, questions, or feedback.

**Hilary Osei-Okrah**  
[LinkedIn](https://www.linkedin.com/in/hilaryoseiokrah) | [GitHub](https://github.com/hilaryoseiokrah)

---

> “Food is culture. AI should respect that.”
