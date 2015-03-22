<<<<<<< HEAD
# Getting-and-Cleaning-Project
## This repository hosts the R code and documentation files for the Data Science's track course "Getting and Cleaning data", available in coursera.  

The dataset being used is: [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)  

## Running the script - run_analysis.R  
- Script should run from the current R working directory 
- Import script run_analysis.R in R studio to run it    

## Within the original zip file, there is a README to learn about the original files, it should be downloaded into your R working directory, both the code book and that file will give you background info about the data
## How the script works - in gory detail
 1. Script is reading data from ./UCI HAR Dataset/
 2. Script needs the following packages to work properly  
			- plyr  
			- dplyr  
			- tidyr  
			- stringr  
 3. It assumes the files are downloaded into a folder called "HCI HAR Dataset" within your R working directory.  
 4. Files used:  
           - "./UCI HAR Dataset/train/subject_train.txt"  
           - "./UCI HAR Dataset/train/X_train.txt"  
           - "./UCI HAR Dataset/train/y_train.txt"  
           - "./UCI HAR Dataset/test/subject_test.txt"  
           - "./UCI HAR Dataset/test/X_test.txt"  
           - "./UCI HAR Dataset/test/y_test.txt"  
           - "./UCI HAR Dataset/activity_labels.txt"  
           - "./UCI HAR Dataset/features.txt"  
           - "./UCI HAR Dataset/features_info.txt"  
           - "./UCI HAR Dataset/README.txt"  
           - "./UCI HAR Dataset/activity_labels.txt" 
 3. The script will read the train files and combine then into 1 file (train) using cbind  
 4. The script will read the test files and combine them into 1 file (test) using cbind  
 5. The script will combine train and test into 1 file (data) using rbind  
 6. The script will read the features.txt file  
 7. The scrip will use features.txt as column names for data, with the addition of names for activity and subject column  
 8. The script will Make Syntactically Valid Names for the data columns  
 9. The script will remove all punctuation characters from data column names  
 10. The script will trim all trailing blanks from data column names  
 11. The script will then create 3 new dataframe, and the recombine them, so that there are only columns that contains mean and std into the resulting file called cleandata  
 12. The activity label file and the cleandata file will be joined by activity  
 13. The column activity will be removed (not needed anymore)
 14. A summary table averaging all columns by subject and activity label will be created, and written to a file called tidysummary.R  within the R working directory   
 15. As needed, the script removes unneeded dataframes, several occurences within script.     

 




=======
Getting and Cleaning Data - Course Project
==========================================

This repository hosts the R code and documentation files for the Data Science's track course "Getting and Cleaning data", available in coursera.

The dataset being used is: [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

## Files

The code takes for granted all the data is present in the same folder, un-compressed and without names altered.

`CodeBook.md` describes the variables, the data, and any transformations or work that was performed to clean up the data.

`run_analysis.R` contains all the code to perform the analyses described in the 5 steps. They can be launched in RStudio by just importing the file.

The output of the 5th step is called `averages_data.txt`, and uploaded in the course project's form.
>>>>>>> 9e4084dc410069ef21d2f78ff1f74b453d239f58
