# Real-Estate-Analytics-Recommendation-Engine

An end-to-end Data Science and Machine Learning application for analyzing the Gurgaon residential real estate market, predicting property prices, and recommending apartments based on location and similarity.

The complete application was built using Streamlit and deployed on AWS.

---

## 📌 Project Overview

Finding the right property requires evaluating multiple factors such as location, price, built-up area, BHK configuration, amenities, and nearby facilities.

This project transforms web-scraped Gurgaon real estate data into an interactive decision-support platform that allows users to:

- Explore the Gurgaon property market
- Analyze sector-wise pricing patterns
- Compare houses and flats
- Estimate property prices using Machine Learning
- Find apartments near a preferred location
- Discover similar apartments using cosine similarity

This is not only a Machine Learning model. It covers the complete Data Science lifecycle:

**Web Scraping → Data Cleaning → EDA → Feature Engineering → Machine Learning → Recommendation System → Streamlit Application → AWS Deployment**

---

## Key Features

### 1. Interactive Real Estate Analytics

The analytics dashboard allows users to explore Gurgaon property data using global filters.

Users can filter properties by:

- Property type
- Sector
- BHK configuration

The dashboard includes:

- Average property price
- Average price per square foot
- Total number of properties
- Average built-up area
- Sector-wise geographical price map
- Area vs price analysis
- Top sectors by average property price
- Top sectors by price per square foot
- BHK distribution
- BHK-wise price range
- House vs flat comparison
- Property price distribution

All visualizations update dynamically according to the selected filters.

---

### 2. Property Price Prediction

A Machine Learning pipeline predicts the estimated market price of a property based on user inputs.

#### Model Inputs

- Property type
- Sector
- Number of bedrooms
- Number of bathrooms
- Number of balconies
- Property age
- Built-up area
- Servant room availability
- Store room availability
- Furnishing type
- Luxury category
- Floor category

#### Output

The model returns an estimated property price range in crores.

The trained preprocessing and prediction workflow is stored as a reusable Machine Learning pipeline.

---

### 3. Two-Stage Apartment Recommendation System

The recommendation system follows a two-stage workflow.

#### Stage 1: Location-Based Filtering

The user selects:

- A preferred location or landmark
- Maximum search radius in kilometres

The system uses a precomputed location-distance matrix to identify apartment projects within the selected radius.

#### Stage 2: Similarity-Based Recommendation

The user selects one apartment from the location-based shortlist.

The selected apartment is then passed to the content-based recommendation engine, which uses cosine similarity to recommend the top 5 most similar apartment projects.

#### Recommendation Flow

**Preferred Location → Radius Filter → Nearby Apartments → User Selection → Cosine Similarity → Top 5 Recommendations**

---

## Data Collection

The dataset used in this project contains residential property information from Gurgaon.

The property data was collected through web scraping and includes information such as:

- Property type
- Sector
- Price
- Price per square foot
- Built-up area
- BHK configuration
- Bathrooms
- Balconies
- Property age
- Furnishing details
- Amenities
- Luxury features
- Floor information
- Apartment projects

The raw scraped data was processed before being used for analysis and Machine Learning.

---

## Data Cleaning and Preprocessing

The preprocessing workflow included:

- Handling missing values
- Removing duplicate records
- Standardizing inconsistent values
- Cleaning numerical features
- Processing categorical variables
- Handling property area information
- Transforming price-related features
- Preparing data for Machine Learning
- Creating model-ready features

---

## Exploratory Data Analysis

EDA was performed to understand important patterns in the Gurgaon real estate market.

The analysis focused on:

- Sector-wise property prices
- Price per square foot
- Property type comparison
- Built-up area and price relationship
- BHK distribution
- BHK-wise price ranges
- Geographic pricing patterns
- Property price distributions

Interactive Plotly visualizations were integrated into the Streamlit application.

---

## Project Architecture

```text
Web Scraping
      ↓
Raw Gurgaon Property Data
      ↓
Data Cleaning & Preprocessing
      ↓
Exploratory Data Analysis
      ↓
Feature Engineering
      ↓
┌─────────────────────────────┐
│                             │
↓                             ↓
Price Prediction       Recommendation System
│                             │
ML Pipeline             Location Filtering
│                             ↓
│                      Cosine Similarity
│                             │
└──────────────┬──────────────┘
               ↓
     Multi-Page Streamlit App
               ↓
         AWS Deployment
Technology Stack
Programming and Data Processing
Python
Pandas
NumPy
Machine Learning
Scikit-learn
Machine Learning Pipelines
Feature Engineering
Recommendation System
Cosine Similarity
Content-Based Recommendation
Location-Based Filtering
Data Visualization
Plotly
Seaborn
Matplotlib
Application Development
Streamlit
Deployment
AWS
Linux
Project Structure
Real-Estate-Analytics-Recommendation-Engine/
│
├── Home.py
│
├── pages/
│   ├── 1_Analytics.py
│   ├── 2_Price_Prediction.py
│   └── 3_Recommendation.py
│
├── datasets/
│   └── processed_property_data.csv
│
├── models/
│   ├── pipeline.pkl
│   ├── location_distance.pkl
│   └── cosine_sim1.pkl
│
├── requirements.txt
└── README.md
```
## Run the Project Locally
1. Clone the repository
git clone https://github.com/Harhjn01/Real-Estate-Analytics-Recommendation-Engine

2. Navigate to the project directory
cd gurgaon-real-estate-intelligence
3. Create a virtual environment
python -m venv venv
4. Activate the virtual environment
Windows
venv\Scripts\activate
Linux/macOS
source venv/bin/activate
5. Install dependencies
pip install -r requirements.txt
6. Run the Streamlit application
streamlit run Home.py

## Deployment
The multi-page Streamlit application was deployed on AWS using a Linux-based cloud environment.

The deployment process included:

Configuring the cloud instance
Setting up the Python environment
Installing project dependencies
Transferring application and model files
Running the Streamlit application on the cloud server
Live Application

deployed application link:

http://3.239.201.121:8501/Analytics
Skills Demonstrated

This project demonstrates practical experience in:

Web Scraping
Data Cleaning
Data Preprocessing
Exploratory Data Analysis
Feature Engineering
Machine Learning
Scikit-learn Pipelines
Recommendation Systems
Cosine Similarity
Interactive Data Visualization
Streamlit Development
Cloud Deployment
AWS
End-to-End Data Science Project Development

## About the Developer

Harsh Jain

I am a final-year student at Maulana Azad National Institute of Technology (MANIT), Bhopal, and a Data Science enthusiast with a strong interest in Machine Learning, Data Analytics, and building end-to-end data-driven applications.

I independently developed this Real Estate Analytics & Recommendation Engine, covering the complete workflow from web scraping and data preprocessing to exploratory analysis, Machine Learning, recommendation system development, Streamlit application development, and AWS deployment.

I enjoy transforming raw data into meaningful insights and building practical Machine Learning systems that users can interact with.

Connect With Me

GitHub:https://github.com/Harhjn01

LinkedIn: https://www.linkedin.com/in/harsh-jain-1725ab26a/

This project is developed for educational and portfolio purposes. Property price predictions are estimates generated by a Machine Learning model and should not be considered professional real estate or financial advice.


Developed by Harsh Jain
