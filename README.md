# To read the TidyDataSet into R:
  `data <- read.table(file_path, header = TRUE); View(data)`
# Description of Data
Detailed description of data can be found in the "Codebook.md" file. Details on the raw data, the cleaning process, and the resulting cleaned data are included.
# Description of run_analysis.R script
## 1. Read in Data
  `Features<-read.table("./features.txt")` ##read in Features data from file
  
  `subjTest<-read.table("./subject_test.txt")` ##read in Test Subject data from file
  
  `subjTrain<-read.table("./subject_train.txt")` ##read in Train Subject data from file
  
  `Xtest<-read.table("./X_test.txt")` ##read in collected Test data from file
  
  `Ytest<-read.table("./y_test.txt")` ##read in Acivity identifiers for test data from file
  
  `Xtrain<-read.table("./X_train.txt")` ##read in collected Train data from file
  
  `Ytrain<-read.table("./y_train.txt")` ##read in Activity identifiers for train data from file
  
  `Activity<-read.table("./activity_labels.txt")` ##read Activity labels from file
## 2.  Clean up Activity Labels and assign to Ytest and Ytrain 
  `Activity$V2<-tolower(Activity$V2)` ##change activity label text to lowercase
  
  `Activity$V2<-gsub("_u","U",Activity$V2)` ##remove underscores and change first letter of second word to uppercase
  
  `Activity$V2<-gsub("_d","D",Activity$V2)` ##remove underscores and change first letter of second word to uppercase
  
  `YtestAct<-sub("1",Activity[1,2],Ytest$V1)` ##assign Activity label #1 (first element in Activity Label vector) to all rows in YtestAct vector that equal 1 and assign the modified Ytest to a new variable, YtestAct
  
  `YtestAct<-sub("2",Activity[2,2],YtestAct)` ##assign Activity label #2 (second element in Activity Label vector) to all rows in YtestAct that equal 2
  
  `YtestAct<-sub("3",Activity[3,2],YtestAct)` ##assign Activity label #3 (third element in Activity Label vector) to all rows in YtestAct that equal 3
  
  `YtestAct<-sub("4",Activity[4,2],YtestAct)` ##assign Activity label #4 (fourth element in Activity Label vector) to all rows in YtestAct that equal 4
  
  `YtestAct<-sub("5",Activity[5,2],YtestAct)` ##assign Activity label #5 (fifth element in Activity Label vector) to all rows in YtestAct that equal 5
  
  `YtestAct<-sub("6",Activity[6,2],YtestAct)` ##assign Activity label #6 (sixth element in Activity Label vector) to all rows in YtestAct that equal 6
  
  `YtrainAct<-sub("1",Activity[1,2],Ytrain$V1)` ##assign Activity label #1 (first element in Activity Label vector) to all rows in Ytrain that equal 1 and assign the modified Ytrain to a new variable, YtrainAct
  
  `YtrainAct<-sub("2",Activity[2,2],YtrainAct)` ##assign Activity label #2 (second element in Activity Label vector) to all rows in YtrainAct that equal 2
  
  `YtrainAct<-sub("3",Activity[3,2],YtrainAct)` ##assign Activity label #3 (third element in Activity Label vector) to all rows in YtrainAct that equal 3
  
  `YtrainAct<-sub("4",Activity[4,2],YtrainAct)` ##assign Activity label #4 (fourth element in Activity Label vector) to all rows in YtrainAct that equal 4
  
  `YtrainAct<-sub("5",Activity[5,2],YtrainAct)` ##assign Activity label #5 (fifth element in Activity Label vector) to all rows in YtrainAct that equal 5
  
  `YtrainAct<-sub("6",Activity[6,2],YtrainAct)` ##assign Activity label #6 (sixth element in Activity Label vector) to all rows in YtrainAct that equal 6
  
## 3. Create Activity label column in original Ytest and Ytrain data.frames
  `Ytest$Activity<-YtestAct` ##create new column "Activity" in Ytest and assign the completed YtestAct variable to it
  
  `Ytrain$Activity<-YtrainAct` ##create new column "Activity" in Ytrain and assign the completed YtrainAct variable to it
  
## 4. Clean up Features to follow Tidy Data rules: no non-alphanumeric characters, descriptive variable names  
  `Features$V2<-gsub("^t|\\(t","Time",Features$V2)` ##replace "t" at beginning of variable name with "Time" to be more descriptive
  
  `Features$V2<-gsub("^f|\\(f","Frequency",Features$V2)` ##replace "f" at beginning of variable name with "Frequency" to be more descriptive
  `Features$V2<-gsub("Acc","Accelerometer",Features$V2)` ##replace "Acc" with more descriptive "Accelerometer"
  
  `Features$V2<-gsub("Gyro","Gyroscope",Features$V2)` ##replace "Gyro" with more descriptive "Gyroscope"
  
  `Features$V2<-gsub("Mag","Magnitude",Features$V2)` ##replace "Mag" with more descriptive "Magnitude"
  
  `Features$V2<-gsub("mean","Mean",Features$V2)` ##replace "mean" with easier to read "Mean"
  
  `Features$V2<-gsub("std","StandardDeviation",Features$V2)` ##replace "std" with more descriptive "StandardDeviation"
  
  `Featurees$V2<-gsub("BodyBody","Body",Features$V2)` ##replace typo "BodyBody" with "Body"
  
  `Features$V2<-gsub("-(.*)\\()-?(.*)|-(.*)-?(.*)","\\1\\2",Features$V2)` ##find and remove dashes around text, and remove "()"
  
  `Features$V2<-gsub("([a-zA-Z]),([0-9])","\\1at\\2",Features$V2)` ##find pattern XYZ,123 and replace the comma with "at"
  
  `Features$V2<-gsub("([a-zA-Z])\\)?,([a-zA-Z])","\\1by\\2",Features$V2)` ##find pattern XYZ,XYZ and replace the comma with "by"
  
  `Features$V2<-gsub("([0-9]+),([0-9]+)","\\1to\\2",Features$V2)` ##find pattern 123,123 and replace the comma with "to"
  
  `Features$V2<-gsub("\\(|\\)$","",Features$V2)` ##remove remaining parentheses that did not match above patterns
  
## 5. Assign tidied Features to Column Names for Xtest and Xtrain  
  `colnames(Xtest)<-Features$V2`
  
  `colnames(Xtrain)<-Features$V2`
  
## 6. Create new Subject column in Xtest and Xtrain and assign Subject identifiers to the new columns  
  `Xtest$Subject<-subjTest[,1]` ##assign test Subject numbers to new column "Subject" in Xtest
  
  `Xtrain$Subject<-subjTrain[,1]` ##assign train Subject numbers to new column "Subject" in Xtrain
  
  `names(Xtest$Subject)<-"Subject"` ##label Subject column
  
  `names(Xtrain$Subject)<-"Subject"` ##label Subject column
  
  `Xtest$SubjectType<-c(rep("test",nrow(Xtest)))` ##create identifier column "SubjectType" for test Subjects in Xtest
  
  `Xtrain$SubjectType<-c(rep("train",nrow(Xtrain)))` ##create identifier column "SubjectType" for train Subjects in Xtrain
  
  `names(Xtest$SubjectType)<-"SubjectType"` ##label SubjectType column
  
  `names(Xtrain$SubjectType)<-"SubjectType"` ##label SubjectType column
  
## 7. Create new Activity column in Xtest and Xtrain  
  `Xtest$Activity<-Ytest$Activity` ##assign Activity labels from Ytest to new column "Activity" in Xtest
  
  `Xtrain$Activity<-Ytrain$Activity` ##assign Activity labels from Ytest to new column "Activity" in Xtest
  
  `names(Xtest$Activity)<-"Activity"` ##label Activity column
  
  `names(Xtrain$Activity)<-"Activity"` ##label Activity column

## 8. Find Columns for Mean and Standard Deviation, merge Xtest and Xtrain
  `MergeCols<-grep("Mean|StandardDeviation|Subject|Activity",names(Xtest))` ##find desired columns by searching for variable names that include Mean, StandardDeviation, Subject, or Activity; assign the column numbers to a vector MergeCols. Because the Columns are in the same order in Xtest and Xtrain, column numbers are pulled from one of data.frames to be used on both
  
  `Merged<-rbind(Xtest[,MergeCols],Xtrain[,MergeCols])` ##create a merged table by rowbinding the columns of Xtest listed in MergeCols to the columns of Xtrain listed in MergeCols
  
## 9. Create a Tidy Data Set from the Merged data.frame  
  `myTidySet<-aggregate(Merged[,1:79],list(Merged$Subject,Merged$Activity),FUN=mean)` ##create a summary table of the Merged data.frame by taking the mean of all of the variable columns and grouping them by both the Subject and Activity columns
  
  `names(myTidySet)[1]<-"Subject"` ##label the Subject column
  
  `names(myTidySet)[2]<-"Activity"` ##label the Activity column
  
  `myTidySet<-myTidySet[order(myTidySet$Subject),]` ##sort the Tidy Data by Subject (ascending) for easier viewing of the data
  
## 10. Write Tidy Data to a text file using write.table
  `write.table(myTidySet,row.names = FALSE,file="myTidySet.txt")` ##write Tidy Data to a text file per course project instructions
