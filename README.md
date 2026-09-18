# SpendPrint AI 2.0

### Predict. Diagnose. Optimize.

SpendPrint AI 2.0 is an ML-powered campaign intelligence platform designed to help companies understand customer campaign response and identify low-response opportunities across products and customer segments.

##  Problem

Companies often send the same marketing campaigns to large groups of customers without knowing which customers are likely to respond or which product/customer combinations are underperforming.

This results in inefficient campaign targeting and wasted marketing effort.

##  Solution

SpendPrint AI 2.0 combines:

**ML Response Prediction**
→ Predict whether a customer is likely to respond to a campaign.

**Model Explanation**
→ Understand which customer features influence the model's prediction.

**Campaign Diagnostics**
→ Identify products and customer segments with relatively low observed campaign response.

**Action Center**
→ Convert these insights into practical campaign testing recommendations.

##  Core Product Flow

Customer Data
↓
ML Response Prediction
↓
Response Probability
↓
Model Explanation
↓
Campaign Diagnostics
↓
Low-Response Opportunities
↓
Recommended Action

## 🤖 Machine Learning

The project uses a trained classification model to predict the campaign response target.

Target:

`Response`

Where:

- `Response = 1` → customer responded to the campaign
- `Response = 0` → customer did not respond

The final trained model and prediction pipeline will be integrated into the application.

##  Dataset Features

The dataset contains customer demographic, purchasing, engagement and campaign-history information including:

- Birth year
- Education
- Marital status
- Income
- Family information
- Recency
- Product spending
- Web purchases
- Catalog purchases
- Store purchases
- Deal purchases
- Web visits
- Previous campaign responses
- Complaints
- Current campaign response

##  Campaign Diagnostics

The system will analyze:

### Product Response

Observed campaign response across product categories such as:

- Wines
- Fruits
- Meat
- Fish
- Sweets
- Gold

### Low-Response Segments

Identify customer groups where campaign response is relatively low.

### Product × Segment Matrix

A heatmap will show observed response patterns across product categories and customer segments.

### Opportunity Alerts

The system highlights situations such as:

High customer activity + Low campaign response

These are treated as opportunities for further investigation rather than proof that a specific product or advertisement caused poor performance.

##  Planned Architecture

React Frontend
↓
FastAPI Backend
↓
ML Prediction Service
↓
Trained ML Model

FastAPI
↓
Campaign Analytics
↓
Supabase PostgreSQL

##  Technology Stack

### Frontend
- React
- Vite
- Tailwind CSS
- Recharts

### Backend
- Python
- FastAPI
- Uvicorn

### Machine Learning
- Scikit-learn
- XGBoost / trained classification model
- Pandas
- NumPy
- Explainability tools where compatible

### Database
- Supabase PostgreSQL

### Development
- Replit
- GitHub
- Figma

##  Project Structure

```text
SpendPrint-AI-2.0/
│
├── README.md
│
├── model/
│   ├── model.pkl
│   ├── features.pkl
│   ├── metrics.json
│   └── predict.py
│
├── data/
│   └── marketing_data.csv
│
├── backend/
│   ├── main.py
│   └── services/
│       ├── model_service.py
│       ├── data_service.py
│       └── diagnostic_service.py
│
└── frontend/
    └── React application
