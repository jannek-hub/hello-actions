# hello-actions

A minimal Flask app to learn GitHub Actions CI/CD.

## Project structure

```
hello-actions/
├── .github/
│   └── workflows/
│       └── ci.yml       ← GitHub Actions pipeline
├── tests/
│   └── test_app.py      ← Pytest tests
├── app.py               ← Flask app
├── requirements.txt
└── README.md
```

## Run locally

```bash
pip install -r requirements.txt
python app.py
# visit http://localhost:5000
```

## Run tests locally

```bash
pytest tests/ -v
```

## How the CI works

Every `git push` to `main` triggers the workflow in `.github/workflows/ci.yml`.  
GitHub spins up a VM, installs dependencies, and runs the tests automatically.  
You can see the results in the **Actions** tab of your repository.
