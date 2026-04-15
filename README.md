README.md - Diet & Health Prediction System
markdown
→Diet & Health Prediction System

A machine learning system that predicts health outcomes based on dietary habits and lifestyle factors.


 →→Overview

This project uses deep learning to predict whether a person is **Healthy**, at **Moderate Risk**, or **High Risk** based on their:

- Diet (calories, sugar, salt, spice level)
- Lifestyle (exercise, sleep)
- Demographics (age, BMI, gender, region)


→→→Quick Start

Option 1: Google Colab (Easiest)

1. Go to [Google Colab](https://colab.research.google.com/)
2. Upload `main_notebook.ipynb`
3. Upload `food_impact_india.csv` when prompted
4. Click **Runtime → Run all**

→→→→Option 2: Local Computer

```bash
 1. Install required packages
pip install numpy pandas scikit-learn tensorflow matplotlib seaborn joblib flask

2. Run the training
python code/train_model.py

3. Start the web app
python api/app.py
Then open http://localhost:5000 in your browser.

 →→→→→Model Performance
Metric	Score
Accuracy	85%
Precision	84%
Recall	        85%
F1-Score	84%
→→→→→→How to Use
1. Python Code
python
from prediction_module import HealthPredictor

 2. Load the model
predictor = HealthPredictor()

3. Your information
my_data = {
    'Age': 45,
    'BMI': 26.5,
    'Daily_Calorie_Intake': 2500,
    'Spice_Level': 'Medium',
    'Diet_Type': 'Vegetarian',
    'Exercise_Level': 'Moderate',
    'Sugar_Intake': 'Medium',
    'Salt_Intake': 'Medium',
    'Gender': 'Female',
    'Region': 'South'
}

4. Get prediction
result = predictor.predict(my_data)

print(f"Health Status: {result['prediction']}")
print(f"Confidence: {result['confidence']:.2%}")

Click "Predict"

5. See your results and recommendations

→→→→→→→→Requirements
1. Python 3.8+

2. TensorFlow 2.10+

3. scikit-learn

4. pandas

5. numpy

6. matplotlib

7. seaborn


→→→→→→→→→Key Findings
1. BMI is the strongest predictor of health

2. Exercise level significantly impacts health outcomes

3. High sugar intake increases health risks

4. Sedentary lifestyle is a major risk factor
