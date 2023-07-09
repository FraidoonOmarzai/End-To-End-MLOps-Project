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

9. **Data Preprocessing Section**
* params.yaml defined
* 02_data_preprocessing.ipynb added
* stage_02_data_preprocessing.py created
* data_preprocessing stage added to dvc.yaml

10. **Model Training Section**
* define params.yaml
* created 03_model_training.ipynb
* mlflow added to the project
```bash
mlflow server \
    --backend-store-uri sqlite:///mlflow.db \
    --default-artifact-root ./artifacts \
    --host 0.0.0.0 -p 1234
```
* stage_03_training_and_evaluation.py created
* model_train_evaluation stage added to dvc pipeline


11. **Log Prediction Model**
* params.yaml defined
* 04_log_production_model.ipynb created
* model_regiseter_name added to stage_03_training_and_evaluation.py
* stage_04_log_production_model.py created
* logg_production_model stage added to dvc
* model with best accuracy loaded in mlflow and saved

