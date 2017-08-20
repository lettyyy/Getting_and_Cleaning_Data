This is for indicating all the variables and summaries calculated, along with unite, and any other relevant information.

Source Data

The information about how the experiment conducted and how the original data collected can be found in the zip file here.

Introduction for the analysis on the original data

"X_train.txt", "y_train.txt" and "subject_train.txt" contain information about training data.
"X_test.txt", "y_test.txt" and "subjuect_test.txt" contain information about testing data.
"features.txt" contains names of all measurements.
Introduction for the code submmited

Using download.file() together with unzip() function to download the zip file from website to my compute.

Using read.table() function to load "X_train.txt", "y_train", "subject_train" in train directory and "X_test", "y_test", "subject_test" into R.

Using rbind() and cbind() functions to merge all train and test data together.

Using read.table() function to load "features.txt" into R.

Using grep() function to find the indexes with "mean()" and "sd()".

select all relevant columns and set the columns name using the selected features name.

Using read.table() function to load "activity_labels.txt" into R.

Using factor() function with arguments "levels = " and "labels = " to replace the numbers to activity names.

Using gsub() function to replace all characters I think they are needed to replace.

Using group_by() and summarise_each() functions in dplyr package to calculate all means for each activity and wach subject.
