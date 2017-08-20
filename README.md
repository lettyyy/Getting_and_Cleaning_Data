Project purpose

The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.

One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the data for the project:

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Ideas behind run_analysis.R

Merges the training and the test sets to create one data set.
 Using download.file() together with unzip() function to download the zip file from website to my compute.
 Using read.table() function to load "X_train.txt", "y_train", "subject_train" in train directory and "X_test", "y_test", "subject_test" into R.
 Using rbind() and cbind() functions to merge all train and test data together.
Extracts only the measurements on the mean and standard deviation for each measurement.
 Using read.table() function to load "features.txt" into R.
 Using grep() function to find the indexes with "mean()" and "sd()". 
 select all relevant columns and set the columns name using the selected features name.
Uses descriptive activity names to name the activities in the data set
 Using read.table() function to load "activity_labels.txt" into R.
 Using factor() function with arguments "levels = " and "labels = " to replace the numbers to activity names.
Appropriately labels the data set with descriptive variable names.
 Using gsub() function to replace all characters I think they are needed to replace.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
 Using group_by() and summarise_all() functions in dplyr package to calculate all means for each activity and wach subject.

Files

run_analysis.R is the R script for running all functions to fulfil this project tasks:
Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
"codebook.md" gives the relevant information about the data and steps to run the project.
"MeanData.txt" is a tidy dataset that contains mean of each measurement for each activity and each subject.
"README.md" is the file you are reading.

