# Customer Churn Prediction API

This is a FastAPI-based web application for predicting customer churn using a pre-trained XGBoost machine learning model. It is designed and ready for deployment on [Render](https://render.com/).

## Tech Stack
- **Web Framework**: FastAPI
- **Machine Learning**: scikit-learn, XGBoost
- **Server**: Uvicorn
- **Frontend**: HTML/Jinja2 (Templates)

## Project Structure
- `app.py`: The main FastAPI application containing the API endpoints and prediction logic.
- `customer_churn_model.joblib`: The pre-trained machine learning model pipeline.
- `requirements.txt`: Python dependencies required to run the application.
- `Procfile`: Command to run the application using Uvicorn.
- `templates/`: Contains HTML templates (e.g., `index.html`) for the frontend interface.
- `static/`: Contains static assets like CSS and JS files for the frontend.

## How to Run Locally

1. **Create and activate a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Start the FastAPI server**:
   ```bash
   uvicorn app:app --reload --host 0.0.0.0 --port 10000
   ```

4. **Access the application**:
   Open your browser and navigate to [http://localhost:10000](http://localhost:10000)

## Deployment on Render

This project is fully configured to be deployed on Render as a Web Service. 

1. Push this directory to a GitHub repository.
2. In the Render Dashboard, create a new **Web Service** and connect your repository.
3. Use the following configuration:
   - **Environment**: `Python 3`
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `uvicorn app:app --host 0.0.0.0 --port $PORT` (or it will automatically use the `Procfile`)
4. Click **Create Web Service**. Render will build and deploy your application automatically.
