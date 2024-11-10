 # Project Overview

The Bay Bridge Real-Time Travel Time Prediction project aims to predict the exact travel time for commuters crossing the Bay Bridge between Oakland and San Francisco. By integrating multiple real-time data sources, such as public transportation GPS, traffic data, weather conditions, and live traffic camera feeds, this project provides accurate travel time predictions and helps commuters make informed travel decisions.

## Key Features:
Real-Time Travel Time Predictions: Uses machine learning models to predict travel time based on current conditions.
Traffic Congestion Detection: Analyzes live traffic camera feeds using object detection techniques (YOLO/Faster R-CNN) to estimate congestion levels.
Weather Impact: Incorporates weather data to predict how conditions like rain, wind, and temperature affect travel time.
Historical Traffic Trends: Uses historical data to understand patterns and seasonal variations.
Commuter Alerts: Sends notifications about expected delays and alternative routes.

## Project Objectives

Reduce Travel Uncertainty: Provide commuters with accurate and up-to-date travel time estimates to improve planning.
Optimize Traffic Management: Support traffic authorities with real-time congestion analysis for better management of the Bay Bridge's traffic flow.
Enhance Commuter Safety: Alert commuters about dangerous weather or road conditions, promoting safer travel.
Encourage Sustainable Transportation: Help commuters make informed choices about public transportation to reduce congestion and environmental impact.

## Technologies Used

**Programming Languages**: Python, JavaScript \
**Machine Learning and Data Analysis**: Scikit-learn, TensorFlow, PyTorch\
**Object Detection and Computer Vision**: OpenCV, YOLO, Faster R-CNN\
**Real-Time Data Handling**: APIs (Google Maps, Waze, OpenWeatherMap, BART, AC Transit)\
**Backend**: Flask or Django (for RESTful APIs and data processing)\
**Frontend**: React, Vue.js (for dashboard and alerts)\
**Data Storage**: PostgreSQL, MongoDB\
**Visualization**: Plotly, Folium, Dash\
**Cloud Hosting**: AWS, GCP\

## Data Sources

- Public Transportation GPS Data: Real-time GPS data from BART, AC Transit, and Muni buses.
- Traffic Data: Live traffic conditions from Google Maps, Waze, and local traffic monitoring services.
- Weather Data: Forecast and current weather conditions from APIs like OpenWeatherMap and Weather Underground.
- Live Traffic Camera Feeds: Real-time images or video feeds from traffic cameras, analyzed using computer vision for congestion detection.

## Key Components

1. Data Collection
Fetch real-time data from public transportation APIs, traffic condition APIs, and weather sources.
Capture live traffic camera footage for object detection and congestion analysis.
2. Data Processing
Clean and preprocess collected data, ensuring it's ready for modeling.
Engineer features such as time of day, weather conditions, historical traffic patterns, and real-time traffic density.
3. Model Development
Implement machine learning models (Random Forest, Gradient Boosting) to predict travel time based on current conditions.
Use deep learning models (LSTM, GRU) to capture temporal dependencies in traffic flow.
Detect vehicles and congestion using object detection algorithms (YOLO or Faster R-CNN) from traffic camera feeds.
4. Real-Time Prediction
Use the trained models to generate real-time travel time predictions based on incoming data.
Provide real-time insights into traffic congestion levels, allowing commuters to adjust their travel plans.
5. Visualization and Dashboard
Develop an interactive dashboard to display real-time predictions, traffic flow, and weather conditions.
Provide heatmaps, congestion visualizations, and alternative route suggestions.
6. Alert System
Implement a notification system to alert users about traffic delays, accidents, or adverse weather conditions.
Provide suggestions for alternative routes or transportation options.

## How to Run the Project

1. Install Dependencies
Ensure you have Python 3.x installed and set up a virtual environment. Then, install the necessary dependencies:
```
pip install -r requirements.txt
```
3. Data Collection
Set up API keys for the various data sources (Google Maps, OpenWeatherMap, etc.). Modify the data_collection.py script to fetch data from the APIs.
4. Model Training
Train the machine learning models using historical traffic data. You can start by training the regression models (Random Forest, Gradient Boosting) for baseline predictions:
```
python train_models.py
```
For deep learning models (LSTM, GRU), use the train_deep_learning.py script.
6. Real-Time Data Processing
To start real-time prediction, run the data ingestion and prediction pipeline:
```
python real_time_prediction.py
```
This will fetch live data, preprocess it, and generate predictions based on the trained models.
8. Running the Dashboard
To launch the interactive dashboard, use:
```
python app.py
```
This will run a Flask app with the dashboard that displays real-time traffic predictions and congestion analysis.
10. Alert System
To set up notifications for delays or congestion, modify the alerts.py script to configure the alert system and integrate with email or push notification services.

## Future Enhancements

- Crowdsourced Data: Allow commuters to report traffic incidents or conditions in real-time via a mobile app, improving the system’s predictive accuracy.
- Multi-Modal Transport: Analyze alternative routes using other modes of transportation (e.g., ferries, bikes) and suggest the best multi-modal route.
- Emergency Alerts: Implement a feature to notify users about emergency events (e.g., accidents, natural disasters) affecting traffic.

## Conclusion

The Bay Bridge Real-Time Travel Time Prediction project integrates cutting-edge machine learning, computer vision, and real-time data processing to provide commuters with accurate travel time predictions, traffic flow insights, and safety alerts. By leveraging APIs, historical data, and live feeds, the project enhances the commuting experience while supporting traffic management and environmental sustainability.
