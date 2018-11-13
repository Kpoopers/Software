# dance-moves-prediction

We aim to predict dance moves using a combination of Random Forest and Support Vector Machine
to get the best possible accuracy. Train and test data are based on the readings obtained
from two sensors (GY-521 MPU6050 3-Axis Acceleration Gyroscope 6DOF Module) attached to the 
dancers wrists. The raw features are Acceleration x, y, z and Rotation x, y, z. There are a
total of 11 dance moves to be classified.

## Resolving Dependencies
1. Create a virtual environment in the directory
  ```shell
  python3 -m venv venv
  ```
2. Activate the virtual environment
  ```shell
  source venv/bin/activate
  ```
3. Install all the required dependencies
  ```shell
  pip install -r requirements.txt
  ```

## Generating Machine Learning Models
1. Activate the virtual environment
2. Resolve all the dependencies
3. Run `python train.py`
4. Find the models in `.sav` format in `models` directory

## Plotting Graphs for All Dance Moves
1. Activate the virtual environment
2. Resolve all the dependencies
3. Make sure that the code below is commented out in `train_data.py` 👎
  ```python
    ##### COMMENT OUT THE CODE BELOW BEFORE RUNNING plot.py #####
    df_max_min = prep.flatten(df, interval)
    df_var = prep.flatten(df, 'var', interval)
    df_concat = prep.concat_df(df_max_min, df_var)
    df = prep.append_truth(df_concat, number)
    #############################################################
  ```
4. Run `python plot.py`
5. Find the graphs in `.png` format in `plots` directory   

## Testing Model
1. Activate the virtual environment
2. Resolve all the dependencies
3. Generate machine learning models
3. Customise how the models generated are utilised in MLModel class (`test_model/__init__.py` file)
4. Run `python test.py`
