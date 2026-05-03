# Heroku Demo

A small Flask machine learning deployment demo for salary prediction. The app loads a serialized regression model, accepts numeric form inputs, and returns a predicted salary through a simple web UI.

## What This Project Shows

- Training a simple regression model with scikit-learn
- Saving the model with `pickle`
- Loading model artifacts in a Flask application
- Rendering predictions through an HTML template
- Deploying a Python web app with a Heroku-style `Procfile`

## Tech Stack

- Python
- Flask
- NumPy
- pandas
- scikit-learn
- Gunicorn

## Repository Structure

```text
.
├── app.py                 # Flask app and prediction route
├── model.py               # Model training script
├── model.pkl              # Serialized model artifact
├── request.py             # Example request script
├── Procfile               # Heroku/Gunicorn process definition
├── requirements.txt
└── templates/
    └── index.html
```

## Run Locally

```bash
git clone https://github.com/sss2107/Heroku-Demo.git
cd Heroku-Demo
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python app.py
```

Open the local URL shown in your terminal, enter the form values, and submit to generate a salary prediction.

## Deployment Notes

The included `Procfile` starts the app with Gunicorn:

```text
web: gunicorn app:app
```

Heroku's free tier has changed since many classic ML deployment demos were created. The same app structure can also be adapted for Render, Railway, Fly.io, AWS Elastic Beanstalk, or a container service.

## Improvement Ideas

- Add the training dataset or document where it comes from
- Move training and inference into separate modules
- Add request validation and user-friendly error messages
- Add a JSON API route for programmatic predictions
- Disable Flask debug mode for production

## License

This project is licensed under the terms in [LICENSE](LICENSE).
