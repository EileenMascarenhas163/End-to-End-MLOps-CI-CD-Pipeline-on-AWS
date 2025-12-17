

# End-to-End MLOps CI/CD Pipeline on AWS
![alt text](.images/10.png)
![alt text](.images/1.png)
![alt text](.images/2.png)
![alt text](.images/3.png)
![alt text](.images/5.png)
![alt text](.images/7.png)
![alt text](.images/8.png)

This project shows how a machine learning model is **trained, tested, deployed, and retrained automatically** using CI/CD on AWS.

The focus is on **production workflow**, not just model training.

---

## What this project does

* Trains an ML model
* Tracks experiments with MLflow
* Tests and validates models
* Builds Docker images
* Deploys model to AWS
* Exposes predictions via API
* Retrains model on schedule

---

## Pipeline Flow

```
Data
 → Training
 → MLflow Tracking
 → Model Evaluation
 → CI/CD Pipeline
 → Docker
 → AWS Deployment
 → Monitoring
 → Retraining
```

---

## Main Components

### Data & Training

* Data loading and basic validation
* Model training using scikit-learn

`src/data/`
`src/models/train.py`

---

### Experiment Tracking

* Logs metrics and parameters
* Stores model versions

MLflow

---

### Model Evaluation

* Compares new model with baseline
* Stops deployment if performance drops

`src/models/evaluate.py`

---

### CI/CD

* Runs tests and training
* Builds Docker image
* Deploys to AWS automatically

GitHub Actions

---

### Deployment

* Dockerized model
* FastAPI inference service
* Runs on AWS (EC2 )

`src/api/`

---

### Monitoring & Retraining

* Logs predictions and errors
* Retrains model using scheduled jobs

---

## Tech Stack

* Python
* Scikit-learn
* MLflow
* FastAPI
* Docker
* GitHub Actions
* AWS

---

