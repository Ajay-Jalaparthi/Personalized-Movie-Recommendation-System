# 🎬 Personalized Movie Recommendation System  

## 📌 Overview  
This project implements a **Personalized Movie Recommendation System** using **Collaborative Filtering** and **Singular Value Decomposition (SVD)**. It leverages the **MovieLens dataset** to analyze user interactions and generate meaningful movie suggestions.  

By applying **dimensionality reduction** with **Truncated SVD** and computing **cosine similarity**, the system predicts and ranks movies tailored to individual users’ preferences. Additionally, it performs **Exploratory Data Analysis (EDA)** to extract insights from the dataset.  

## 🚀 Features  
✅ **Data Processing:** Loads and cleans the MovieLens dataset  
✅ **Exploratory Data Analysis (EDA):** Visualizes data distributions and trends  
✅ **User-Item Matrix:** Constructs a sparse matrix for collaborative filtering  
✅ **Dimensionality Reduction:** Implements **Truncated SVD** for better performance  
✅ **Movie Recommendations:** Uses **cosine similarity** to generate personalized suggestions  
✅ **Visualization:** Includes **word clouds, correlation heatmaps, and rating distributions**  

## 📊 Dataset  
The project uses the **MovieLens (ml-latest-small)** dataset, which consists of:  
- **100,836** ratings from **610** users across **9,742** movies  
- Each movie has metadata including **title** and **genres**    

### 🔍 Dataset Info  

```python
# Ratings Dataset
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 100836 entries, 0 to 100835
Data columns (total 4 columns):
 #   Column     Non-Null Count   Dtype  
---  ------     --------------   -----  
 0   userId     100836 non-null  int64  
 1   movieId    100836 non-null  int64  
 2   rating     100836 non-null  float64  
 3   timestamp  100836 non-null  int64  
dtypes: float64(1), int64(3)
memory usage: 3.1 MB

# Movies Dataset
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 9742 entries, 0 to 9741
Data columns (total 3 columns):
 #   Column   Non-Null Count  Dtype 
---  ------   --------------  ----- 
 0   movieId  9742 non-null   int64 
 1   title    9742 non-null   object  
 2   genres   9742 non-null   object  
dtypes: int64(1), object(2)
memory usage: 228.5+ K
```

## 🛠️ Tech Stack  
🔹 **Python** – Core language  
🔹 **Pandas & NumPy** – Data manipulation  
🔹 **Matplotlib & Seaborn** – Data visualization  
🔹 **Scikit-learn** – Machine learning (SVD & cosine similarity)  
🔹 **SciPy (csr_matrix)** – Sparse matrix handling  
🔹 **WordCloud** – Genre visualization  

## 📌 Implementation Steps  
### **1️⃣ Load and Process Data**  
- Downloads the MovieLens dataset  
- Reads **ratings.csv** and **movies.csv**  
- Prepares the **user-item matrix**  

### **2️⃣ Exploratory Data Analysis (EDA)**  
- **Visualizes rating distributions** using histograms  
- **Identifies most rated movies**  
- **Generates a word cloud** for popular genres  
- **Creates a correlation matrix** for movie interactions  

### **3️⃣ Collaborative Filtering with SVD**  
- **Transforms user-item matrix** into a compressed form  
- **Applies Truncated SVD** to reduce dimensionality  
- **Computes cosine similarity** to find similar movies  

### **4️⃣ Generate Personalized Recommendations**  
- Predicts movie preferences for a given user  
- Ranks top **10 movie recommendations**  

## 🎯 Sample Results  
### **Top 10 Recommended Movies for a Sample User**  
| Movie ID | Title |  
|----------|-----------------------------------------------------|  
| 260      | Star Wars: Episode IV - A New Hope (1977) |  
| 589      | Terminator 2: Judgment Day (1991) |  
| 1196     | Star Wars: Episode V - The Empire Strikes Back (1980) |  
| 1197     | The Princess Bride (1987) |  
| 1198     | Raiders of the Lost Ark (1981) |  
| 1200     | Aliens (1986) |  
| 1210     | Star Wars: Episode VI - Return of the Jedi (1983) |  
| 1240     | The Terminator (1984) |  
| 2028     | Saving Private Ryan (1998) |  
| 2571     | The Matrix (1999) |  
 
## 📈 Visualizations  

### 1️⃣ Rating Distribution  
- Analyzes the distribution of user ratings across all movies  
- Helps understand user preferences and rating tendencies  
![alt text](image-1.png)

### 2️⃣ Most Rated Movies  
- Identifies movies with the highest number of ratings  
- Provides insights into popular films in the dataset  
![alt text](image-2.png)

### 3️⃣ Movie Genre Word Cloud  
- Generates a word cloud representation of movie genres  
- Highlights the most common genres in the dataset visually  
![alt text](image-3.png)"# Personalized-Movie-Recommendation-System" 
