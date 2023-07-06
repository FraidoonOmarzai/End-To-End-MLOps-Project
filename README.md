# End-To-End-MLOps-Project


```bash
## MLOps Lifecycle:

    1. Problem Definition and Requirement Gathering
    2. EDA
    3. Feature Engineering
    4. Feature Selection
    5. Model Creation
    6. Model Hyper-parameter Tunning
    7. Model Deployment
    8. Retraining Approaches
```

## Steps:

1. Git clone the repository and Define template of the project

```bash
touch template.py
python3 template.py
```

2. define setup.py scripts (**The setup.py** is a module used to build and distribute Python packages. It typically contains information about the package)


3. Create environment and install dependencies

```bash
conda create -n mlops-env python=3.9 -y
conda activate mlops-env
pip install -r requirements.txt
```

4. define logger (**The Logging** is a means of tracking events that happen when some software runs)

5. define utils (**The utils.py** makes it easy to execute common tasks in Python scripts)

6. **Data Ingesstion Section**
 * constants added
 * params.yaml defined
 * 01_data_ingeston.ipynb created
 * stage_01_data_ingeston.py created
 * data downloaded

7. **DVC Section**
 * run dvc init
 * define data_ingeston stage in dvc.yaml
 * run dvc repro

8. **EDA**
 * load the dataset
 * statistical checking
 * checking number of unique values for each columns
 * check data type
 * check duplicate values
 * check null values
 * check balance of the dataset
 * check outliers
 * visualization
 * checking correlation
