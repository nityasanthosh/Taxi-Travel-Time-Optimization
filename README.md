cat > README.md << 'EOF'
#  Taxi Travel Time Optimization using Ant Colony & Genetic Algorithms

This project focuses on optimizing **taxi travel time** in New York City by combining **machine learning** and **bio-inspired algorithms**. The problem is modeled as a **Traveling Salesman Problem (TSP)**, where the goal is to determine the most efficient route connecting multiple pickup and drop-off locations.

To achieve this, I used an **XGBoost model** to predict travel times between locations and applied **Ant Colony Optimization (ACO)** and **Genetic Algorithm (GA)** techniques to minimize total travel duration.

---

##  Project Overview

### 🔹 Step 1: Data Preparation & Analysis
- Used NYC Taxi Trip Duration Dataset (2016) from [Kaggle](https://www.kaggle.com/c/nyc-taxi-trip-duration/data).  
- Cleaned and analyzed raw data to identify key travel patterns.  
- Extracted relevant features like distance, timestamp, coordinates, and vendor details.

### 🔹 Step 2: Predictive Modeling
- Trained an **XGBoost regression model** to predict travel time between pickup and drop-off coordinates.  
- Saved the trained model as `xgb_model.sav` for reuse in optimization steps.

### 🔹 Step 3: Route Optimization
- Implemented **Ant Colony Optimization (ACO)** and **Genetic Algorithm (GA)** to explore route combinations.
- Both algorithms iteratively improved route efficiency using simulated biological behavior and evolutionary principles.
- The goal was to find **the path with minimum total predicted travel time**.

---

##  Project Structure

├── .gitattributes # Git LFS tracking for large files
├── README.md # Project documentation
├── xgb_model.sav # Trained XGBoost model file
│
├── Bio_Inspired_Algorithms/
│ ├── aco_main.ipynb # Ant Colony Optimization implementation
│ └── genetic_algo_main.ipynb # Genetic Algorithm implementation
│
├── Figures/ # Contains output figures and visualizations
│
├── Util_functions/
│ ├── xgboost.ipynb # Travel time prediction model
│ └── basic_analysis/
│ ├── basic_analysis.ipynb # Exploratory data analysis
│ └── cleaned_data.xlsx # Preprocessed dataset


---

##  Requirements

Install the dependencies before running any notebooks:

```bash
pip install numpy pandas matplotlib xgboost geopy
```

Usage
1️. Data Analysis

Explore and preprocess data:
```bash
Open Util_functions/basic_analysis/basic_analysis.ipynb
```
2️. Model Training

Train and save the XGBoost model:
```bash
Open Util_functions/xgboost.ipynb
```
3️. Route Optimization

Run evolutionary algorithms:
```bash
Open Bio_Inspired_Algorithms/aco_main.ipynb
Open Bio_Inspired_Algorithms/genetic_algo_main.ipynb
```
## Outputs

- Predicted travel times between routes
- Optimized travel paths and cost convergence plots
- Saved model file (xgb_model.sav) for reuse

# Example route convergence:

| Algorithm               | Visualization                                |
| ----------------------- | -------------------------------------------- |
| Ant Colony Optimization |  Progressive path improvement                |
| Genetic Algorithm       |  Evolutionary convergence to optimal route   |

## Future Enhancements

- Combine ACO and GA into a hybrid optimizer for faster convergence.
- Integrate real-time traffic data for dynamic predictions.
- Build a web-based dashboard to visualize optimized routes interactively.


