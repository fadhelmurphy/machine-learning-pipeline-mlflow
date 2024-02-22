# Implement MLFlow to existing model

- Tracking Cross-validation, Hyperparameter Tuning, evaluation metric
- Generate REST API with MLFlow
- Manage Stage (Staging & Production)

## Installation

`
pip install mlflow scikit-learn numpy pandas seaborn
`

## Run notebook

first thing, you have to clone this project by this command below.

`git clone git@github.com:fadhelmurphy/machine-learning-pipeline-mlflow.git`

### VSCODE

if you're using vscode editor you can this project folder or you can open this project by command below.
```
code machine-learning-pipeline-mlflow
```

### Jupyter Notebook
if you're using jupyter notebook you can try this command down below to open the notebook

```
cd machine-learning-pipeline-mlflow
jupyter notebook MLflow-example-notebook.ipynb
```

after you run all cells from this notebook, you can open the MLFlow dashboard or REST API by port down below.

`localhost:3000` : MLFlow Dashboard (you can open this on your browser)

`localhost:3001` : MLFlow REST API

## Inference Request

this is curl example to predict regression data by MLFlow API

```
curl --silent --show-error --location 'http://localhost:3001/invocations' \
--header 'Content-Type: application/json' \
--data '{
    "inputs": {
        "season": 4.0,
        "yr": 1.0,
        "mnth": 12.0,
        "hr": 20.0,
        "holiday": 0.0,
        "weekday": 2.0,
        "workingday": 1.0,
        "weathersit": 2.0,
        "temp": 0.5,
        "atemp": 0.4848,
        "hum": 0.63,
        "windspeed": 0.2239
    }
}'
```