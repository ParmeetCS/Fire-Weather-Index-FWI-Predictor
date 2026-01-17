# 🔥 Fire Weather Index (FWI) Predictor

A machine learning web application that predicts the Fire Weather Index (FWI) using environmental and meteorological parameters. Built with Flask and powered by Ridge Regression.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Flask](https://img.shields.io/badge/Flask-2.0+-green.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-orange.svg)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Details](#model-details)
- [API Endpoints](#api-endpoints)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

The Fire Weather Index (FWI) is a numeric rating of fire intensity used by fire agencies worldwide. This application uses machine learning to predict FWI based on weather conditions, helping in early fire risk assessment and prevention.

## ✨ Features

- **Real-time Predictions**: Get instant FWI predictions based on input parameters
- **User-friendly Interface**: Modern, responsive web interface
- **ML-Powered**: Utilizes Ridge Regression for accurate predictions
- **9 Input Parameters**: Comprehensive weather and environmental analysis

## 📊 Dataset

This project uses the **Algerian Forest Fires Dataset** which contains data from two regions in Algeria:
- Bejaia region (northeast)
- Sidi Bel-abbes region (northwest)

The dataset includes fire weather observations and the Fire Weather Index (FWI) components.

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/fire-weather-index-prediction.git
   cd fire-weather-index-prediction
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python application.py
   ```

5. **Access the application**
   
   Open your browser and navigate to: `http://127.0.0.1:5000`

## 💻 Usage

1. Navigate to the home page
2. Click on "Start Prediction" button
3. Enter the required weather parameters:
   - **Temperature (°C)**: Current temperature
   - **RH (%)**: Relative Humidity
   - **Ws (km/h)**: Wind Speed
   - **Rain (mm)**: Rainfall amount
   - **FFMC**: Fine Fuel Moisture Code
   - **DMC**: Duff Moisture Code
   - **ISI**: Initial Spread Index
   - **Classes**: Fire class (0 or 1)
   - **Region**: Region code (0 or 1)

4. Click "Calculate Fire Weather Index"
5. View the predicted FWI value

## 📁 Project Structure

```
ML Project Implementation/
│
├── application.py          # Main Flask application
├── requirements.txt        # Python dependencies
├── README.md              # Project documentation
│
├── models/
│   ├── ridge.pkl          # Trained Ridge Regression model
│   └── scalar.pkl         # Fitted StandardScaler
│
├── notebooks/
│   ├── Algerian_forest_fires_dataset_UPDATE.csv  # Dataset
│   ├── ML.ipynb           # Machine Learning experiments
│   └── Model_training.ipynb  # Model training notebook
│
└── templates/
    ├── index.html         # Landing page
    └── home.html          # Prediction form page
```

## 🤖 Model Details

### Algorithm
- **Model**: Ridge Regression
- **Preprocessing**: StandardScaler for feature normalization

### Input Features
| Feature | Description | Unit |
|---------|-------------|------|
| Temperature | Air temperature | °C |
| RH | Relative Humidity | % |
| Ws | Wind Speed | km/h |
| Rain | Rainfall | mm |
| FFMC | Fine Fuel Moisture Code | - |
| DMC | Duff Moisture Code | - |
| ISI | Initial Spread Index | - |
| Classes | Fire classification | 0/1 |
| Region | Geographic region | 0/1 |

### Output
- **FWI (Fire Weather Index)**: A numeric rating representing fire intensity

## 🔗 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Landing page |
| `/predictdata` | GET | Prediction form |
| `/predictdata` | POST | Submit prediction request |

## 📸 Screenshots

### Landing Page
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/495dbf4c-d746-47bd-9b14-d4bbdb014805" />

### Prediction Form
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/d8c991c4-a07c-4135-b2d7-6144388b9493" />

### Results
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/48800f2a-346f-4b55-8565-d07fabccf715" />


## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 🙏 Acknowledgments

- Algerian Forest Fires Dataset
- scikit-learn library
- Flask framework

---

<p align="center">
  Made with ❤️ for fire safety and prevention
</p>
