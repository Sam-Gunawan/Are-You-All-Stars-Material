# 🌟 Are You All-Stars Material? — Predicting NBA Stardom with Machine Learning

What does it really take to be an NBA All-Star?  
This project transforms that iconic question into a **data science challenge**, fusing real player stats with handcrafted models to predict who has what it takes to shine under the spotlight.

Using division-level data and a roster of confirmed All-Stars, we build and evaluate machine learning models that identify rising stars—and maybe even the overlooked legends in the making.

> 🧠 This isn't just stat-chasing. It's basketball meets machine learning—with a side of storytelling.

---

## 🏀 Project Summary

### 🎯 Goal
To build a **predictive model** that determines whether a player is “All-Star material” based on in-game performance metrics.

### 🗃️ Dataset
- Player statistics from **7 NBA divisions**: Atlantic, Central, Southeast, Northwest, Southwest, Pacific
- A reference `All_Stars.csv` with players who made it into the All-Star list
- Features include: Points per Game, Assists, Rebounds, FG%, 3PT%, Turnovers, and more

---

## 🧠 Machine Learning Pipeline

### 🧼 Data Preprocessing
- Combined all division-level CSVs into one cohesive dataset
- Standardized player names and matched them to the All-Star roster
- Standardized data types (the weight and height of players)

### 🧪 Similarity-Based Modeling with KNN

We approached the classification problem using a single, clean method: **K-Nearest Neighbors (KNN)**. This algorithm determines whether a player is an All-Star by comparing them to other players using different similarity measures.

Three distinct **distance metrics** were evaluated:

- 📐 **Euclidean Distance** – Measures straight-line distance in the feature space  
- 🔄 **Cosine Similarity** – Captures the angle between stat vectors, emphasizing stat distribution over magnitude  
- 🧭 **Mahalanobis Distance** – Considers both scale and correlation of features for more nuanced similarity

> Each metric was used with the same KNN model to compare how each perspective on "similarity" affects classification accuracy.

---

## 📊 Evaluation Metrics

The performance of each model configuration was assessed using two core metrics:

- **Accuracy**: The proportion of all correct predictions
- **Precision**: The proportion of predicted All-Stars who were actually All-Stars

These simple yet powerful metrics helped us compare how effective each distance measure was in identifying real All-Stars without overfitting or overcomplicating the problem.

---

## 📁 File Overview

```
.
├── players_dataset     # Raw stats from each NBA division
    ├── All_Stars.csv   # Ground-truth All-Star player list
    ├── Atlantic.csv
    ├── Central.csv
    ├── Northwest.csv
    ├── Pacific.csv
    ├── Southeast.csv
    └── Southwest.csv
├── all_stars_ml.ipynb  # Complete ML pipeline with model training and testing
├── README.md           # You are here!
```

---

## 📊 Key Findings

- Players with **well-rounded stats** (points + assists + rebounds + good FG%) had the highest All-Star probability
- Several underrated players emerged with All-Star-caliber stats but lacked prior recognition

---

## 👥 Team Members & Roles

| Name                   | Role                          |
|------------------------|-------------------------------|
| Samuel T. Gunawan      | Project Manager               |
| [Priska A. Likarsa](https://github.com/priskaaimee)      | Developer, Data Analyst       |
| [Jorel A. Setiabudi](https://github.com/jorelalexander)     | Developer, Data Analyst       |
| [Evan A. Chandra](https://github.com/shifinn)        | Developer, Data Analyst       |

> _Looking to grow the team. We’re always open to data collabs. Interested in AI + sports analytics? Reach out!_

---

## 🌱 Future Works

Here’s where the court leads next:

- 🧠 **XGBoost & Neural Nets**: Add advanced models to improve performance
- 🌐 **Web App**: Streamlit interface for users to input stats and get predictions
- 📊 **Live API**: Pull current-season data from NBA APIs for real-time All-Star predictions
- 🏷️ **Explainability**: Use SHAP values to explain model predictions for each player
- 📈 **Player Trendline Tracker**: Predict future All-Star probability based on recent performance


---

## 🤝 Let’s Connect

- 🧒 [Instagram – Samuel Gunawan](https://www.instagram.com/sam__gunawan/)
- 👩 [Instagram - Priska Aimee](https://www.instagram.com/priskaaimee_/)
- 🧒 [Instagram - Jorel Alexander](https://www.instagram.com/jorel.setiabudi/)
- 🧒 [Instagram - Evan Aditya Chandra](https://www.instagram.com/evan_aditya_c/)
- 💻 [More Projects](https://github.com/Sam-Gunawan)

---

> *"Great players don’t just show up in stat sheets. But that’s where they start."*

This project aims to bridge the narrative of sports with the science of prediction one model at a time.
