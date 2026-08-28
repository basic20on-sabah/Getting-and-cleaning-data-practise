# CodeBook

## Overview

This CodeBook describes the variables, data, and transformations
Performed for the Getting and Cleaning Data course project.

The project uses the Human Activity Recognition Using Smartphones
(UCI HAR Dataset).

## Original Data

The original dataset contains measurements collected from
Smartphones worn by subjects while performing activities.

The data are divided into training and test sets.

The main files used are:

- `features.txt`
- `activity_labels.txt`
- `train/X_train.txt`
- `train/y_train.txt`
- `train/subject_train.txt`
- `test/X_test.txt`
- `test/y_test.txt`
- `test/subject_test.txt`

## Variables in the Final Dataset

### subject

Identifies the subject who performed the activity.

There are 30 subjects in the dataset.

### activity

Identifies the activity performed by the subject.

The activity names are:

1. WALKING
2. WALKING_UPSTAIRS
3. WALKING_DOWNSTAIRS
4. SITTING
5. STANDING
6. LAYING

### Measurement Variables

The final dataset contains measurements related to:

- Body acceleration
- Gravity acceleration
- Body gyroscope
- Frequency-domain measurements

Only measurements containing `mean()` or `std()` in the original
Feature names were selected.

The final dataset contains 66 measurement variables in addition
To `subject` and `activity`, resulting in 68 variables in total.

## Transformations

The following transformations were performed:

### 1. Merge Training and Test Data

The training and test datasets were combined to create one dataset.

### 2. Select Mean and Standard Deviation Measurements

Only measurements corresponding to mean and standard deviation
Were selected using the original feature names.

### 3. Use Descriptive Activity Names

Activity numbers were replaced with descriptive activity names
Using `activity_labels.txt`.

### 4. Rename Variables

Variable names were made more descriptive.

Examples include:

- `t` → `Time`
- `f` → `Frequency`
- `Acc` → `Accelerometer`
- `Gyro` → `Gyroscope`
- `mean()` → `Mean`
- `std()` → `Std`

### 5. Create the Tidy Dataset

The selected measurements were grouped by:

- subject
- activity

The mean of each selected measurement was then calculated for
Each subject and activity combination.

## Final Dataset

The final file is:

`tidy_data_average.txt`

It contains:

- 180 observations
- 68 variables
- 30 subjects
- 6 activities

There is one row for each combination of subject and activity.

The final dataset contains no missing values.

## Output

The final tidy dataset is written using:

`write.table()`

And saved as:

`tidy_data_average.txt`
