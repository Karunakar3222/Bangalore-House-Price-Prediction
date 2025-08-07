# 🏠 Bangalore House Price Predictor

[](https://opensource.org/licenses/MIT)
[](https://www.python.org/)
[](https://flask.palletsprojects.com/)
[](https://scikit-learn.org/)

A comprehensive machine learning project that predicts house prices in Bangalore. This repository covers the entire pipeline from data cleaning and feature engineering to model training and deployment as a web application.

-----

## 📋 Table of Contents

  - [Project Overview](https://www.google.com/search?q=%23-project-overview)
  - [Key Features](https://www.google.com/search?q=%23-key-features)
  - [Tech Stack](https://www.google.com/search?q=%23-tech-stack)
  - [Project Architecture](https://www.google.com/search?q=%23-project-architecture)
  - [Installation & Setup](https://www.google.com/search?q=%23-installation--setup)
  - [Usage](https://www.google.com/search?q=%23-usage)
  - [Model Performance](https://www.google.com/search?q=%23-model-performance)
  - [Project Learnings](https://www.google.com/search?q=%23-project-learnings)
  - [License](https://www.google.com/search?q=%23-license)
  - [Contact](https://www.google.com/search?q=%23-contact)

-----

## 📖 Project Overview

The real estate market is complex and dynamic. This project aims to simplify price prediction for properties in Bangalore by leveraging machine learning. Using a dataset of Bangalore housing listings, we perform extensive data preprocessing to handle missing values and outliers, engineer new features to improve accuracy, and train a regression model. The final model is wrapped in a Flask API and presented through a user-friendly web interface where users can input property details and receive an estimated price.

-----

## 🔑 Key Features

  - **Data Cleaning:** Robust techniques to handle missing data, inconsistent formatting, and duplicates.
  - **Outlier Detection & Removal:** Statistical methods to identify and remove price-distorting outliers.
  - **Feature Engineering:** Creation of new features like `price_per_sqft` to enhance model performance.
  - **Regression Modeling:** Implementation and evaluation of multiple regression algorithms to find the best fit.
  - **Interactive Web UI:** A clean and simple web interface built with Flask for easy interaction with the model.
  - **End-to-End Deployment:** The entire application is containerized and deployed on a cloud platform (Render).

-----

## 🛠️ Tech Stack

  - **Backend:** Python, Flask
  - **ML/Data Science:** Scikit-learn, Pandas, NumPy, Matplotlib
  - **Deployment:** Render, Gunicorn
  - **Version Control:** Git & GitHub

-----

## 🏗️ Project Architecture

The project follows a standard machine learning application workflow:

```
1. Data Collection       (Bengaluru House Data.csv)
      |
      v
2. Data Preprocessing    (Jupyter Notebook: data cleaning, feature engineering)
      |
      v
3. Model Training        (Jupyter Notebook: training Linear Regression, Lasso, etc.)
      |
      v
4. Model Serialization   (Exporting the trained model to a .pickle file)
      |
      v
5. API & UI Development  (Flask server `app.py`, HTML/CSS frontend)
      |
      v
6. Deployment          (Deploying the Flask app on Render)
```

-----

## 🚀 Installation & Setup

To run this project locally, follow these steps:

1.  **Install Dependencies**

    ```bash
    pip install -r requirements.txt
    ```

2.  **Run the Application**

    ```bash
    python app.py
    ```

3.  **Access the App**
    Open your web browser and navigate to `http://127.0.0.1:5000`.

-----

## 💡 Usage

Once the application is running, you can predict a house price by:

1.  Selecting a location from the dropdown menu.
2.  Entering the total square feet of the property.
3.  Choosing the number of Bathrooms and Bedrooms (BHK).
4.  Clicking the **"Predict Price"** button to see the estimated price in lakhs.

-----

## 📊 Model Performance

Several regression models were tested, with **Lasso Regression** providing the best results after hyperparameter tuning.

  - **Evaluation Metric:** R² Score (Coefficient of Determination)
  - **Test Set R² Score:** `~0.82`

This score indicates that the model can explain approximately 82% of the variance in house prices, making it a reliable predictor.

-----

## 📚 Project Learnings

  - **The Power of Preprocessing:** The quality of input data directly dictates model performance. A significant portion of this project was dedicated to cleaning and structuring the dataset, which was a critical learning experience.
  - **Feature Engineering is Key:** Simple features like location and size are important, but engineered features like `price_per_sqft` were instrumental in removing outliers and improving model accuracy.
  - **Deployment Challenges:** Transitioning from a local Jupyter Notebook to a deployed web application involves its own set of challenges, including dependency management, environment configuration, and ensuring application stability.

-----

## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

-----

## 📝 License

This project is distributed under the MIT License. See the `LICENSE` file for more information.

-----

python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`