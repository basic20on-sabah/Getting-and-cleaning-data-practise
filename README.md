# Getting and Cleaning Data Course Project
This repository contains the required code and documentation for the Coursera Getting and Cleaning Data course project.

## Files Included:
1. `run_analysis.R`: The R script that downloads, cleans, merges the data, and calculates the final averages.
2. `tidy_data_average.txt`: The final tidy data set containing the average of each variable for each activity and each subject.
3. `CodeBook.md`: Description of the variables, data, and transformations.

## How the Script Works:
1. Downloads and unzips the dataset.
2. Merges the training and the test sets to create one data set.
3. Extracts only the measurements on the mean and standard deviation for each measurement.
4. Uses descriptive activity names to name the activities in the data set.
5. Appropriately labels the data set with descriptive variable names.
6. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
