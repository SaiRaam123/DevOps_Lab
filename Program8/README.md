# ML Project Environment Setup (Commands Only — No Code Files Included)

## 1️⃣ Create and activate virtual environment
```
python3 -m venv venv
source venv/bin/activate
```
---
## 2️⃣ Install required ML packages
(You will create **requirements-ml.txt** separately)
```
pip install -r requirements-ml.txt
```

---

## 3️⃣ Verify installed packages
```
pip freeze | grep -E "numpy|pandas|scikit-learn|jupyter"
```

---

## 4️⃣ Create and run the Jupyter notebook
(You will create **ml_setup.ipynb** separately)

Start Jupyter:
```
jupyter lab
```
---
## CODE to write in Jupyter Notebook
```
import numpy as np
import pandas as pd
from sklearn.linear_model import LinearRegression

print("numpy:", np.__version__)
print("pandas:", pd.__version__)

# tiny sample dataset
X = np.array([[1], [2], [3], [4]])
y = np.array([2, 4, 6, 8])

model = LinearRegression().fit(X, y)

print("coef:", model.coef_)
print("intercept:", model.intercept_)
```
---

## 5️⃣ Commit notebook + requirements file to Git
```
git add requirements-ml.txt ml_setup.ipynb
git commit -m "Add ML environment requirements and verification notebook"
git push origin main
```
