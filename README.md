# End-to-End-Books-Recommender-System
End-to-end book recommendation system built with collaborative filtering

## Workflow

- config.yaml
- entity
- config/configuration.py
- components
- pipeline
- main.py
- app.py

# How to run?

### 1. Clone the Repository
```bash
git clone https://github.com/albertomonterom/End-to-End-Books-Recommender-System.git
cd ai-medical-chatbot
```

### 2. Create a virtual environment
```bash
python -m venv books
```

Activate it

```bash
source books/bin/activate   # Linux/Mac
books\Scripts\activate      # Windows
```

### 3. Install Requirements
```bash
pip install -r requirements.txt
```

Now run,
```bash
streamlit run app.py
```