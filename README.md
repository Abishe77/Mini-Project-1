# Mini-Project 1
That’s a good instinct. A clean, human, professional README always feels stronger than something overly decorated. Here’s a natural, portfolio-ready version you can use:

---

# Social Service Recommendation System

Content-Based Recommendation using Euclidean Distance

## Overview

This project implements a simple content-based recommendation system that suggests relevant social services (Food, Shelter, Hospital) based on user preferences.

The system represents both user input and services as feature vectors and computes similarity using Euclidean distance. Services with smaller distance scores are considered better matches and are ranked accordingly.

## Problem Statement

Given:

* A desired service type
* Maximum travel distance
* Preferred minimum working hours

The system recommends the top five most relevant services from the dataset.

## Methodology

### Data Preprocessing

* One-hot encoding of the `Type` column (Food, Shelter, Hospital)
* Normalization of:

  * Distance relative to the user's maximum travel distance
  * Working hours scaled to a 0–1 range

### Feature Representation

Each service is represented as:

[Food, Shelter, Hospital, Distance_norm, Hours_norm]

The user input is converted into a corresponding feature vector.

### Similarity Computation

* Euclidean distance is calculated using scikit-learn.
* Smaller distance indicates a closer match.
* Services are sorted in ascending order of distance score.

### Visualization

A 2D scatter plot is generated using Matplotlib to:

* Display all services in feature space
* Represent the user as a reference point
* Highlight the top five recommended services
* Illustrate the geometric interpretation of distance-based recommendation

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

## How to Run

1. Clone the repository:
   git clone https://github.com/Abishe77/Mini-Project-1

2. Install required dependencies:
   pip install pandas numpy scikit-learn matplotlib

3. Run the script:
   python recommendation_system.py

4. Provide:

   * Desired service type
   * Maximum travel distance
   * Preferred working hours

The system will display the top five recommended services and generate a visualization.

## Future Improvements

* Implement cosine similarity for comparison
* Introduce weighted feature importance
* Apply dataset-wide Min-Max scaling
* Build a simple web interface using Streamlit
* Deploy as a web-based application

## Learning Outcome

This project demonstrates the foundational principles behind recommendation systems, including feature engineering, vector space representation, and distance-based similarity metrics. It highlights how meaningful recommendations can be generated using mathematical concepts without relying on complex models.



