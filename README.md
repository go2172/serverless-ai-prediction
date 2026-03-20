# serverless-ai-prediction
Serverless AI project for predicting exam scores using AWS Lambda, API Gateway, and S3 frontend.
# 🎯 EduPredict – Serverless AI Exam Score Predictor

EduPredict is a serverless machine learning application that predicts student exam scores based on study behavior and performance metrics. This project demonstrates deploying an ML model using AWS services without relying on traditional servers.


## 🚀 Live Application

🌐 **Frontend (S3 Website):**  
  https://gowtham-serverless-lab.s3.us-east-1.amazonaws.com/index.html

- 🔗 **API Endpoint:**  
  https://ls1b888pma.execute-api.us-east-1.amazonaws.com/predict

## 🧠 Features

- Predicts exam scores based on:
  - Hours studied
  - Attendance percentage
  - Previous grade
  - Assignments completed
  - Extra classes
- Serverless backend using AWS Lambda
- REST API using API Gateway
- Static frontend hosted on AWS S3
- No EC2 instances used (fully serverless)

---

## 🏗️ Architecture
User → S3 (Frontend) → API Gateway → Lambda → ML Model (model.pkl)


---

## 🛠️ Technologies Used

- Python (Machine Learning Model)
- AWS Lambda
- AWS API Gateway
- AWS S3 (Static Hosting)
- HTML, JavaScript (Frontend)

## 📂 Project Structure
├── index.html # Frontend dashboard
├── model.pkl # Trained ML model
├── lambda_function.py # Backend logic (Lambda)
├── README.md # Project documentation


---

## ⚙️ How It Works

1. User enters input values on the web dashboard
2. Frontend sends a POST request to API Gateway
3. API Gateway triggers AWS Lambda
4. Lambda loads the trained model (`model.pkl`)
5. Model processes input and returns prediction
6. Result is displayed on the dashboard

---

## 🧪 Sample Input

```json
{
  "hours_studied": 5,
  "attendance_pct": 80,
  "previous_grade": 75,
  "assignments_done": 8,
  "extra_classes": 1
}

{
  "predicted_score": 82.5
}

