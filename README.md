Of course\! Based on the files you've provided, here is a comprehensive README file for your GitHub repository.

-----

# Crop & Fertilizer Recommendation System

## 📖 Overview

This project is a web-based application designed to assist farmers in making data-driven decisions. It provides recommendations for the most suitable crop to cultivate based on various environmental and soil parameters. Additionally, the project includes a model for recommending the appropriate type of fertilizer to use.

The primary goal is to increase agricultural productivity and help farmers choose the right crop for their specific land conditions, leading to better yields and profitability.

-----

## ✨ Features

  - **Crop Recommendation:** Recommends the optimal crop based on:
      - Nitrogen (N), Phosphorus (P), and Potassium (K) content in the soil.
      - Climatic conditions like Temperature and Humidity.
      - Soil pH value.
      - Rainfall level.
  - **Fertilizer Recommendation:** Suggests the right fertilizer based on soil and crop type. (Model and notebook included).
  - **User-Friendly Web Interface:** An intuitive web UI built with Flask and Bootstrap for easy input of parameters.
  - **Machine Learning Powered:** Utilizes a Random Forest Classifier for crop prediction and a Decision Tree for fertilizer prediction, trained on comprehensive agricultural datasets.

-----

## 💻 Technology Stack

  - **Backend:** Python, Flask
  - **Frontend:** HTML, CSS, Bootstrap
  - **Machine Learning:** Scikit-learn, Pandas, NumPy
  - **Jupyter Notebook** for model development and analysis.

-----

## 📊 Datasets

This project utilizes two primary datasets:

1.  **`Crop.csv`**: Contains data on soil metrics (N, P, K, pH) and environmental conditions (temperature, humidity, rainfall) for 22 different crops.
2.  **`Fertilizer.csv`**: Contains data on soil conditions, crop types, and the corresponding fertilizer recommendations.

-----

## 🤖 Models

Two machine learning models were trained for this project:

1.  **Crop Recommendation Model (`best_crop_model.pkl`):**

      - **Algorithm:** Random Forest Classifier
      - **Purpose:** Predicts the most suitable crop from 22 options based on 7 input features.
      - **Training Details:** See the `crop (2).ipynb` notebook for the complete workflow, including data preprocessing, model training, and evaluation.

2.  **Fertilizer Recommendation Model (`fertilizer_model.sav`):**

      - **Algorithm:** Decision Tree Classifier
      - **Purpose:** Recommends a fertilizer type based on soil and crop data.
      - **Training Details:** The training process is detailed in the `Fertilizer_recommendation (1).ipynb` notebook.

-----

## 🚀 Setup and Installation

To run this project locally, follow these steps:

**1. Clone the repository:**

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

**2. Create and activate a virtual environment (recommended):**

```bash
# For Windows
python -m venv venv
venv\Scripts\activate

# For macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

**3. Install the required dependencies:**
Create a file named `requirements.txt` and add the following lines:

```
Flask
numpy
pandas
scikit-learn
```

Then run the installation command:

```bash
pip install -r requirements.txt
```

**4. Ensure model files are named correctly:**
The Flask application (`app.py`) expects the following model files. Please rename them if necessary:

  - `best_crop_model.pkl` -\> `model.pkl`
  - The scalers used in `app.py` (`standscaler.pkl`, `minmaxscaler.pkl`) should be generated from the `crop (2).ipynb` notebook. Make sure to save them with these names after training.

**5. Run the Flask application:**

```bash
python app.py
```

**6. Open your browser:**
Navigate to `http://127.0.0.1:5000` to see the application live.

-----

## kullanımı How to Use

1.  Open the web application in your browser.
2.  You will see a form with input fields for Nitrogen, Phosphorus, Potassium, Temperature, Humidity, pH, and Rainfall.
3.  Fill in the values based on your soil and environmental data.
4.  Click the **"Get Recommendation"** button.
5.  The application will process the inputs and display the name of the recommended crop.

  ---

## 📁 File Structure

```
├── app.py                      # Main Flask application script
├── templates/
│   └── index.html              # Frontend HTML template
├── static/
│   └── img.jpg                 # Image used in the UI
├── best_crop_model.pkl         # Trained model for crop recommendation (rename to model.pkl)
├── standscaler.pkl             # Standard scaler object
├── minmaxscaler.pkl            # Min-Max scaler object
├── crop (2).ipynb              # Jupyter Notebook for crop model training
├── Crop.csv                    # Dataset for crop recommendation
├── fertilizer_model.sav        # Trained model for fertilizer recommendation
├── fertilizer_scaler.sav       # Scaler for fertilizer model
├── Fertilizer_recommendation (1).ipynb # Jupyter Notebook for fertilizer model training
├── Fertilizer.csv              # Dataset for fertilizer recommendation
├── requirements.txt            # List of Python dependencies
└── README.md                   # This file
```

-----

## 🤝 Contributing

Contributions are welcome\! If you have ideas for improvements or find any issues, please open an issue or submit a pull request.

-----
