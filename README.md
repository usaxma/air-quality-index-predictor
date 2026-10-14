# Air Quality Index Predictor

Regress daily air-quality index from pollutant and weather features, then serve predictions from a Flask app.

The training notebook compares classical models with **TPOT** AutoML. The deployed model is an XGBoost regressor.

## Skills

- Tabular regression and feature engineering
- XGBoost
- TPOT genetic AutoML
- Model serialization (`pickle`)
- Flask inference on a held-out year (`real_2018.csv`)

## Dataset

Training data: `notebooks/AQI_Data.csv`  
Inference sample: `app/real_2018.csv`

## Run the notebook

```bash
pip install -r requirements.txt
jupyter notebook notebooks/Air_Quality_Index_Predictor.ipynb
```

## Run the app

```bash
cd app
pip install -r ../requirements.txt
python app.py
```

Open `http://127.0.0.1:5000`, then submit to score the 2018 sample.

## Structure

```
air-quality-index-predictor/
├── notebooks/
│   ├── Air_Quality_Index_Predictor.ipynb
│   └── AQI_Data.csv
├── app/
│   ├── app.py
│   ├── aqi_XGBreg_model.pkl
│   ├── real_2018.csv
│   └── templates/
├── requirements.txt
└── README.md
```
