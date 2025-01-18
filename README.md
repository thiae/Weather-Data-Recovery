# Weather-Data-Recovery
A deep learning project focused on recovering missing daily weather measurements from sequential datasets. The project involves visualizing, preprocessing, and training a neural network to impute missing values in historical weather data.


# 🌤️ Sequential Weather Data Recovery

## Project Overview
This repository contains my solution to an assessment to recover missing weather data from sequential datasets. The project focuses on designing a neural network architecture capable of imputing missing daily measurements of weather variables over four decades. The dataset includes corrupted and uncorrupted weather data for training and a test dataset with only corrupted data.

---

## 🧾 Problem Statement
The goal is to recover missing values in weather variables such as temperature, precipitation, pressure, and more. This is critical for ensuring the reliability of historical weather data and enabling accurate predictions for future weather patterns.

### Dataset
The dataset includes the following columns:
- `date`: The date of each observation.
- `cloud_cover`: Cloud cover in percentage.
- `sunshine`: Hours of sunshine recorded.
- `global_radiation`: Global radiation in W/m².
- `max_temp`: Maximum daily temperature in °C.
- `mean_temp`: Mean daily temperature in °C.
- `min_temp`: Minimum daily temperature in °C.
- `precipitation`: Precipitation in mm.
- `pressure`: Atmospheric pressure in hPa.

The data is organized as follows:
- `training_set/`: Contains three decades of data in separate `.csv` files, each with corrupted and uncorrupted versions.
- `test_set.csv`: Contains the fourth decade of corrupted data, with missing values to be imputed.

---

## 📋 Project Objectives
1. **Data Visualization**:
   - Plot time series for each variable, showing trends and missing data for one decade.
   - Generate histograms to compare variable distributions before and after corruption.

2. **Data Preparation**:
   - Create PyTorch `TensorDataset` and `DataLoader` for the training and test datasets.
   - Pair corrupted data with corresponding uncorrupted labels for training.

3. **Model Design and Training**:
   - Design and train a neural network to recover missing weather data.
   - Evaluate the architecture’s performance on the test set using line plots of filled-in values.

4. **Output and Save Results**:
   - Save the recovered test data into `test_set_nogaps.csv` in the same format as the original test_set.csv file.

---

## 🛠️ Methodology
1. **Exploratory Data Analysis (EDA)**:
   - Visualize trends and corruption in the training and test datasets.
   - Compare variable distributions to understand the extent of data corruption.

2. **Data Preprocessing**:
   - Prepare PyTorch `TensorDataset` and `DataLoader` for training and testing.
   - Structure data for batch-wise training of the neural network.

3. **Model Architecture**:
   - Design a neural network architecture tailored to sequential data imputation.
   - Train the model from scratch (no pre-trained networks allowed).

4. **Evaluation and Output**:
   - Visualize imputed test data and save the results in the required format.

---

## 📝 Deliverables
1. **Code**:
   - Python implementation for data loading, visualization, preprocessing, and model training.
2. **Visualizations**:
   - Line plots and histograms showing data trends and corruption.
3. **Model**:
   - Trained neural network to recover missing weather data.
4. **Output File**:
   - Recovered test data saved as `test_set_nogaps.csv`.

---

## 🎯 Key Takeaways
This repository demonstrates the ability to:
- Work with sequential data in the context of deep learning.
- Design and train custom neural networks for data imputation.
- Communicate results effectively through clear documentation and visualizations.

---

## 📂 Repository Structure
- `README.md`: Overview and project description (this file).
- `training_set/`: Training data containing corrupted and uncorrupted weather variables across three decades.
- `test_set.csv`: Corrupted test data for the fourth decade.
- `notebooks/`: Jupyter notebooks for data visualization, preprocessing, model design, and training.
- `results/`: Contains the `test_set_nogaps.csv` file with recovered weather data.
- `models/`: Saved models and architecture details.

---

Feel free to reach out with any inquiries or for clarification!
