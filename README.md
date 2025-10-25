# DataClustering_
### Capacitated K-Center on NYC 911 EMS Data

This repository explores clustering methods for **emergency facility location optimization** in New York City.  
The project investigates how **capacity constraints** (like limited ambulances per station) affect traditional clustering objectives such as *K-Center*  to handle them efficiently.
---
## Overview
Emergency response systems rely on locating service centers optimally to minimize response time.  
However, real-world centers have **limited capacity** — each can handle only a certain number of incidents.  

This project:
- Analyzes NYC 911 EMS incident data.
- Implements **Capacitated K-Center** algorithm.
- Introduces **binary search-based bounding** for finding minimal feasible radius.
- Compares unconstrained vs. capacity-constrained clustering.
- Visualizes cluster assignments on a city map using **GeoPandas** and **Folium**.

## 🧮 Tech Stack

| Category | Tools / Libraries |
|-----------|------------------|
| **Languages** | Python (3.9+) |
| **Data** | Pandas, GeoPandas, NumPy |
| **Visualization** | Folium, Matplotlib |
| **Algorithms** | scikit-learn (K-Means), custom K-Center + flow assignment |
| **Environment** | Google Colab / Jupyter Notebooks |

## 🧑‍💻 Author
**Srihari Tadala**  
Master’s in Computer Science, Portland State University  
Focus: AI
Advisor - Sayan Bandyapadhyay
Assistant Professor  
Dept. of Computer Science at Portland State University 
