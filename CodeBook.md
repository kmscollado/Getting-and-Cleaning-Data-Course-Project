# Getting and Cleaning Data Course Project
Getting and Cleaning Data Course Project



The script processes raw data set into a tidy data for analysis. The following variables are described below:

subject_train: Subject who performed the activity

y_train: Training Labels

X_train: Training Set 

subject_test: Subject who performed the activity

y_test: Test Labels

X_test: Test Set

data_merged: Merged train and test data set

ftrs: Names of measurement

mean_std: Matching columns

data_mean_std: Data with the matching columns of mean and std

data_extracted: Data extracted using mean and standard deviation with subject and activity

activity_labels: Name of the activity

data_tidy: Final data set




The script runs as follows:

1. MERGE the train and the test sets to create one data set.
  
    - Set the working directory.
    - Create a directory if it does not exist.
    - Download the file.
    - Unzip the downloaded file.
    - Read the dataset into R. 
    - Merge train and test sets.
    - Assign column names to the merged dataset.

2. EXTRACT only the measurements on the mean and standard deviation for each measurement.

    - Find the columns that match.
    - Extract using the previously matched indices.

3. USE descriptive activity names to name the activities in the data set.

    - Read the labels into R.
    - Name the activities.    

4. LABEL appropriately the data set with descriptive variable names.

    - View the default names.
    - Modify the names by fixing the characters.   
    - View modified names and check if all names are described.
    
5. From the data set in step 4, CREATE a second, independent tidy data set with the average of each variable for each activity and each subject.

    - Load the needed package "dplyr".
    - Create a second data set: (1)grouping by subject and activity and (2)getting the mean.
    - Create a text file to save the tidy data set "data_tidy.txt". 
    
    
    
The script processes data with the following information (taken from the README.txt of the UCI HAR Dataset folder) :

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.
  
