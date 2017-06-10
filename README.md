The run_analysis.R script reads data from the "Human Activity Recognition Using Smartphones Dataset Version 1.0" and produces a new - tidy - dataset.

In this project, data collected from the accelerometer and gyroscope of the Samsung Galaxy S smartphone was retrieved, worked with, and cleaned, to prepare a tidy data that can be used for later analysis.

This repository contains the following files:

README.md - File which provides an overview of the data set and how it was created.
tidy_data.txt, which contains the data set.
CodeBook.md, the code book, which describes the contents of the data set (data, variables and transformations used to generate the data).
run_analysis.R, the R script that was used to create the data set.


The original dataset included the following data files:
1.features.txt': List of all features.

2.activity_labels.txt': List of class labels and their activity name.

3.train/X_train.txt': Training set.

4.train/y_train.txt': Training labels.

5.train/subject_train.txt': ID's of subjects in the training data

6.test/X_test.txt': Test set.

7.test/y_test.txt': Test labels.

8.test/subject_test.txt': ID's of subjects in the training data


Project Summary:

You should create one R script called run_analysis.R that does the following.

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

A brief description of the script:

The run_analysis.R script merges data from a number of .txt files and produces a tidy data set which may be used for further analysis.
1.Reads all required .txt files and labels the datasets
2.The appropriate activity id and subjectid are appended to the "test" and the "training" data, which are then combined into one single data frame
3.Using the "grep" function, all the columns with mean() and std() values are extracted and then a new data frame is created.This data frame will include only the "activity", the "subject" and the mean() and std() columns.
4.Aggregate function is used to Create a second, independent tidy data set with the average of each variable for each activity and each subject (averages_data).
5. write.table function is used to wite the averages_data from step 4 into a tidy data text file.
