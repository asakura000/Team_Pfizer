# team_pfizer

## Help I don't know how to add our large dataset to our github so here is the google link:

### Original dataset: PfizerTurnoverPredictionModel.csv
### Modified dataset: Pfizer_Turnover_Prediction_Model_version2.csv
    - Changes made:
      1. Converted 'RandomID' column to int type, and moved it to the front (first column after the index)
      2. For columns 'POS_LEVEL1', 'POS_LEVEL2', 'POS_LEVEL3', 'POS_LEVEL4', 'POS_LEVEL5':
          a. converted data type to string
          b. added leading '0' characters where the string is less than 8 characters long
      3. Added a 'Year' column to help in data imputation later for Country Level data 
      
## When you import the 'Pfizer_Turnover_Prediction_Model_version2.csv' file, please use the following code to maintain the string datatypes for the POSLEVEL columns:
df = pd.read_csv('Pfizer_Turnover_Prediction_Model_version2.csv', converters={'POS_LEVEL1': lambda x: str(x), 'POS_LEVEL2':lambda x: str(x),
                                          'POS_LEVEL3': lambda x: str(x), 'POS_LEVEL4': lambda x: str(x),
                                          'POS_LEVEL5': lambda x: str(x)})
