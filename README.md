# 📊 Zomato Data Analysis

This project focuses on cleaning and preprocessing raw Zomato restaurant data to prepare it for analysis and visualization. The dataset contains various attributes of restaurants listed on Zomato, such as name, location, cost, cuisines, ratings, and more.

## 📁 Project Structure

```
zomato_data_analysis/
├── zomato_data_cleaning.ipynb   # Jupyter notebook for data cleaning
├── zomato_clean_data.csv        # Cleaned dataset saved after processing
└── README.md                    # Project documentation
```

## 📌 Objectives

- Clean and preprocess raw Zomato data.
- Remove irrelevant and redundant columns.
- Handle missing and inconsistent values.
- Normalize and standardize data types for future analysis.
- Export the cleaned dataset for further use in analytics or machine learning tasks.

## 🧹 Data Cleaning Process

The data cleaning workflow includes:

1. **Importing Libraries**
   - Used `pandas` and `numpy` for data manipulation and cleaning.

2. **Loading the Dataset**
   - Loaded the raw Zomato dataset using `pandas.read_csv()`.

3. **Dropping Unnecessary Columns**
   - Removed non-informative or redundant columns such as:
     - `url`, `address`, `phone`, `dish_liked`, `menu_item`, `reviews_list`, etc.

4. **Renaming Columns for Clarity**
   - Renamed:
     - `rate` → `rating`
     - `approx_cost(for two people)` → `cost_per_person`
     - `listed_in(type)` → `restaurant_type`
     - `name` → `restaurant_name`

5. **Handling Duplicates**
   - Dropped all duplicate rows from the dataset.

6. **Handling Missing and Inconsistent Values**
   - Removed rows with missing `cuisines` or `cost_per_person`.
   - Defined a custom function to process `rating` values and convert them into floats.
   - Filled missing `rating` values with the column's mean.

7. **Data Type Conversion**
   - Converted relevant columns to `string` for consistency.
   - Cleaned `cost_per_person` column by removing commas and converting to integer.

8. **Saving the Cleaned Dataset**
   - Exported the cleaned data to a new CSV file: `zomato_clean_data.csv`.

## 🛠️ Tools & Technologies Used

- Python 🐍
- Jupyter Notebook 📓
- Pandas
- NumPy

## 🔮 Next Steps

- Perform Exploratory Data Analysis (EDA).
- Visualize insights such as:
  - Most popular cuisines.
  - Average ratings by location.
  - Distribution of online orders vs. table bookings.
- Apply clustering or predictive models based on user ratings and cost.

## 📌 How to Run

1. Clone the repository or download the files.
2. Make sure `zomato.csv` (raw dataset) is present in the same directory.
3. Open `zomato_data_cleaning.ipynb` in Jupyter Notebook.
4. Run all cells to clean the data.
5. The cleaned file `zomato_clean_data.csv` will be saved in the same directory.

## 📬 Contact

For feedback, queries, or collaborations, feel free to reach out!