# # Covid-19 CDC Dataset Analysis and Predictions

## Data Quality Plan:

### Observations:

- The data sample contains 12 columns and 10 000 rows
- The type for all the features is 'object' and needs to be changed to datetime and category
- There are no numeric values
- All the features are categorical, there are no continuous features in the data set
- The data sample contains duplicates that have to be dropped
- The data sample contains a high number of Null, Unknown or Missing values for multiple features

### Summary of data quality plan:

| Variable Names                     | Data Quality Issue            | Handling Strategy              |
|------------------------------------|-------------------------------|--------------------------------|
| cdc_case_earliest_dt               | OK                            | Do Nothing                     |
| cdc_report_dt                      | Deprecated                    | Remove                         |
| pos_spec_dt                        | Null values                   | Do Nothing                     |
| onset_dt                           | Missing or Unknown Values     | Merge Missing and Unknown      |
| current_status                     | OK                            | Do Nothing                     |
| sex                                | Missing or Unknown Values     | Drop Missing and Unknown       |
| age_group                          | Missing or Unknown Values     | Drop Missing and Unknown       |
| race_ethnicity_combined            | Missing or Unknown Values     | Merge Missing and Unknown      |
| hosp_yn                            | Missing or Unknown Values     | Merge Missing and Unknown      |
| icu_yn                             | Missing or Unknown Values     | Merge Missing and Unknown      |
| death_yn                           | OK                            | Do Nothing                     |
| medcond_yn                         | Missing or Unknown Values     | Merge Missing and Unknown      |


## Contents:
 1. Preparing Data Quality Report for the provided CSV file.
- Read CSV
- Check shape
- Check first rows
- Check last rows
- Check the data types
- Check info for each feature
- Check column names
- Check cardinality
- Print description tables
- Check for duplicates and drop them if needed
- Save the cleaned data

2. Data preparation
- Encoding target feature (death_yn)
- Randomly shuffle the rows of your dataset and split the dataset into two datasets: 70% training and 30% test.
- Plot the correlations between all the categorical features.
- Interpreting features paired with `death_yn`
- Drop features that are not needed
- Convert the categorical variables into dummies variable to allow modeling
- Remove the redundant dummies which contain no additional information
- Set up the train test split again based on the dataset with the dummies included

3. Linear Regression
4. Logistic Regression
5. Random Forest
6. Model Improvement
