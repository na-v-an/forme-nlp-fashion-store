# FORME — NLP Clothing Review Store

A Flask clothing catalogue and customer-review application developed for RMIT COSC2820 Assignment 3, Milestone II.

## Features

- Clothing and category listings sourced from the supplied course dataset
- Search with plural/singular term normalization
- Product detail pages showing existing reviews
- Review form with star rating and text
- Recommendation prediction from a Milestone I CountVectorizer + Logistic Regression classifier
- Customer override of predicted labels
- SQLite review persistence and individually accessible review pages
- Responsive dark fashion-store interface

## Local setup

Requires Python 3.11+ and the **complete project files** (including `data/` and `models/`).

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pytest tests -q
python -m flask --app app run --port 5050
```

Open http://127.0.0.1:5050.

## Project structure

- `app.py` — Flask routes and storage
- `nlp.py` — NLP inference and preprocessing
- `train_model.py` — retraining script
- `templates/` — Jinja UI
- `static/` — CSS and visual assets
- `data/` — course data and preprocessing resources
- `models/` — trained classifier
- `tests/` — test suite
- `README.txt` — assignment notes

**Note:** GitHub Pages cannot execute a Python/Flask server. This is a source repository; a live public website requires a Python hosting service.

**Academic-materials notice:** Do not publish course-provided or assessed materials publicly without checking your course's sharing rules.
