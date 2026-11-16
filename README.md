Customer Analytics Data Warehouse
Experiment 2 - Data Preprocessing Using Python
Project overview
This experiment prepares the Bank Customer Churn dataset for further data analysis and machine learning. The preprocessing workflow follows the steps in the supplied experiment document: inspect the dataset, handle missing values, remove duplicate records, remove identifier columns, encode categorical features, and standardize numerical features.

Project name: Customer Analytics Data Warehouse
Dataset: Bank Customer Churn Prediction (Churn_Modelling.csv)
Target column: Exited (1 = customer exited, 0 = customer stayed)
The dataset name is retained as Bank Customer Churn because it identifies the actual source dataset. Customer Analytics Data Warehouse is the project title.

Objectives
- Load the Bank Customer Churn dataset using Python.
- Identify and handle missing values.
- Identify and remove duplicate records.
- Encode categorical values into numerical form.
- Standardize numerical features using StandardScaler.
- Save a clean dataset for further analysis and machine learning.
Tools and libraries
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook, Google Colab, or a terminal
Dataset columns used
The source dataset includes RowNumber, CustomerId, Surname, CreditScore, Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary, and Exited.

RowNumber, CustomerId, and Surname are removed from the feature set because they are identifiers. Exited is kept separately as the target variable. Geography and Gender are encoded using One-Hot Encoding.
Project files
- Customer_Analytics_Data_Warehouse_Experiment_2.docx - updated, editable experiment document.
- Customer_Analytics_Data_Warehouse_Experiment_2.pdf - PDF version of the experiment document.
- customer_analytics_data_preprocessing.py - executable Python preprocessing program.
- README.md - project documentation.
Setup
1. Install Python 3.x.
2. Open a terminal in the project folder.
3. Install the required libraries:
   python -m pip install pandas numpy scikit-learn
4. Download or obtain the Bank Customer Churn CSV dataset used for the experiment.
5. Place Churn_Modelling.csv in the project folder, or note its full file path.
Run the program
python customer_analytics_data_preprocessing.py Churn_Modelling.csv
To choose a different output file:
python customer_analytics_data_preprocessing.py Churn_Modelling.csv --output preprocessed_customer_data.csv
The program prints the original dataset preview, dataset information, missing-value counts, duplicate count, final dataset preview, final shape, and validation counts. It saves the cleaned and transformed data to preprocessed_customer_data.csv.
Preprocessing workflow
1. Load dataset: Read the CSV file into a Pandas DataFrame.
2. Check missing values: Use isnull().sum() to count missing values in each column.
3. Handle missing values: Fill missing numerical values with the column mean and missing categorical values with the most frequent value (mode).
4. Remove duplicates: Count repeated rows and remove them using drop_duplicates().
5. Remove identifier columns: Drop RowNumber, CustomerId, and Surname from the feature set.
6. Separate features and target: Store input attributes in X and Exited in y.
7. Encode categorical data: Apply One-Hot Encoding to Geography and Gender.
8. Scale numerical features: Apply StandardScaler to numerical input features.
9. Save and verify: Recombine the features with Exited, check missing values and duplicates, and write the result to CSV.
Expected output
A file named preprocessed_customer_data.csv containing the encoded and standardized input features alongside the original Exited target column. The script reports the final shape, total missing values, and duplicate-row count.
Result
The Bank Customer Churn dataset is preprocessed for the Customer Analytics Data Warehouse by handling missing values, removing duplicate records, encoding categorical attributes, and standardizing numerical features. The resulting dataset is ready for further analysis and machine learning.
