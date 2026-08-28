# Getting and Cleaning Data Course Project

This repository contains my solution for the Coursera
Getting and Cleaning Data course project.

## Dataset

The project uses the Human Activity Recognition Using Smartphones
Dataset (UCI HAR Dataset).

The dataset contains measurements collected from the accelerometers
And gyroscopes of smartphones worn by subjects while performing
Different activities.

## Files

-	`run_analysis.R` - R script used to download, read, merge, clean,
  And summarize the data.
-	`tidy_data_average.txt` - Final tidy dataset containing the average
  Of each selected measurement for each subject and activity.
-	`CodeBook.md` - Describes the data, variables, and transformations.

## How the Script Works

The `run_analysis.R` script performs the following steps:

1. Downloads and unzips the UCI HAR Dataset.
2. Reads the training and test data.
3. Merges the training and test sets.
4. Extracts only measurements related to the mean and standard
   Deviation.
5. Uses descriptive activity names instead of activity numbers.
6. Appropriately labels the variables with descriptive names.
7. Creates a second tidy dataset containing the average of each
   Selected variable for each subject and each activity.
8. Writes the final dataset to `tidy_data_average.txt`.

## Output

The final tidy dataset contains:

- 180 observations
- 68 variables
- 30 subjects
- 6 activities

Each row represents one subject performing one activity.

The six activities are:

- WALKING
- WALKING_UPSTAIRS
- WALKING_DOWNSTAIRS
- SITTING
- STANDING
- LAYING
