# Description of Raw Data: taken directly from Features_Info.txt of zipped data file
Description of Cleaned Data can be found at the end of this file.
## Feature Selection 
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

## These signals were used to estimate variables of the feature vector for each pattern:  ('-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.)

  tBodyAcc-XYZ

  tGravityAcc-XYZ

  tBodyAccJerk-XYZ

  tBodyGyro-XYZ

  tBodyGyroJerk-XYZ

  tBodyAccMag

  tGravityAccMag

  tBodyAccJerkMag

  tBodyGyroMag

  tBodyGyroJerkMag

  fBodyAcc-XYZ

  fBodyAccJerk-XYZ

  fBodyGyro-XYZ

  fBodyAccMag

  fBodyAccJerkMag

  fBodyGyroMag

  fBodyGyroJerkMag


## The set of variables that were estimated from these signals are: 

  mean(): Mean value

  std(): Standard deviation

  mad(): Median absolute deviation 

  max(): Largest value in array

  min(): Smallest value in array

  sma(): Signal magnitude area

  energy(): Energy measure. Sum of the squares divided by the number of values. 

  iqr(): Interquartile range 

  entropy(): Signal entropy

  arCoeff(): Autorregresion coefficients with Burg order equal to 4

  correlation(): correlation coefficient between two signals

  maxInds(): index of the frequency component with largest magnitude

  meanFreq(): Weighted average of the frequency components to obtain a mean frequency

  skewness(): skewness of the frequency domain signal 

  kurtosis(): kurtosis of the frequency domain signal 

  bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window.

  angle(): Angle between to vectors.


## Additional vectors obtained by averaging the signals in a signal window sample. These are used on the angle() variable:

  gravityMean

  tBodyAccMean

  tBodyAccJerkMean

  tBodyGyroMean

  tBodyGyroJerkMean
  
# Description of Cleaned Data:
## Feature Selection
Mean (mean()) and Standard Deviation (std()) features were selected for inclusion in the Tidy Data Set. The variable meanFreq() was included in this set, as it represents a weighted mean of the frequency variable data.

## Variable Names: Changes made to Feature Labels
1. Dashes and parentheses were removed
2. Each word was Capitalized for ease of reading
3. Typographic error "BodyBody" was corrected to "Body
4. "Gyro" was changed to "Gyroscope"
5. "Acc" was changed to "Accelerometer"
6. "Mag" was changed to "Magnitude"
7. "std" was changed to "StandardDeviation"
8. "t" at the beginning of a variable was changed to "Time"
9. "f" at the beginning of a variable was changed to "Frequency"

## Variables present in Cleaned Data, with raw vs cleaned variable names ('-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.)
Raw Data | Cleaned Data
------------ | -------------
tBodyAcc-mean()-XYZ | TimeBodyAccelerometerMeanXYZ
tBodyAcc-std()-XYZ | TimeBodyAccelerometerStandardDeviationXYZ
tGravityAcc-mean()-XYZ | TimeGravityAccelerometerMeanXYZ
tGravityAcc-std()-XYZ | TimeGravityAccelerometerStandardDeviationXYZ
tBodyAccJerk-mean()-XYZ | TimeBodyAccelerometerJerkMeanXYZ
tBodyAccJerk-std()-XYZ | TimeBodyAccelerometerJerkStandardDeviationXYZ
tBodyGyro-mean()-XYZ | TimeBodyGyroscopeMeanXYZ
tBodyGyro-std()-XYZ | TimeBodyGyroscopeStandardDeviationXYZ
tBodyGyroJerk-mean()-XYZ | TimeBodyGyroscopeJerkMeanXYZ
tBodyGyroJerk-std()-XYZ | TimeBodyGyroscopeJerkStandardDeviationXYZ
tBodyAccMag-mean() | TimeBodyAccelerometerMagnitudeMean
tBodyAccMag-std() | TimeBodyAccelerometerMagnitudeStandardDeviation
tGravityAccMag-mean() | TimeGravityAccelerometerMagnitudeMean
tGravityAccMag-std() | TimeGravityAccelerometerMagnitudeStandardDeviation
tBodyAccJerkMag-mean() | TimeBodyAccelerometerJerkMagnitudeMean
tBodyAccJerkMag-std() | TimeBodyAccelerometerJerkMagnitudeStandardDeviation
tBodyGyroMag-mean() | TimeBodyGyroscopeMagnitudeMean
tBodyGyroMag-std() | TimeBodyGyroscopeMagnitudeStandardDeviation
tBodyGyroJerkMag-mean() | TimeBodyGyroscopeJerkMagnitudeMean
tBodyGyroJerkMag-std() | TimeBodyGyroscopeJerkMagnitudeStandardDeviation
fBodyAcc-mean()-XYZ | FrequencyBodyAccelerometerMeanXYZ
fBodyAcc-std()-XYZ | FrequencyBodyAccelerometerStandardDeviationXYZ
fBodyAcc-meanFreq()-XYZ | FrequencyBodyAccelerometerMeanFreqXYZ
fBodyAccJerk-mean()-XYZ | FrequencyBodyAccelerometerJerkMeanXYZ
fBodyAccJerk-std()-XYZ | FrequencyBodyAccelerometerJerkStandardDeviationXYZ
fBodyAccJerk-meanFreq()-XYZ | FrequencyBodyAccelerometerJerkMeanFreqXYZ
fBodyGyro-mean()-XYZ | FrequencyBodyGyroscopeMeanXYZ
fBodyGyro-std()-XYZ | FrequencyBodyGyroscopeStandardDeviationXYZ
fBodyGyro-meanFreq()-XYZ | FrequencyBodyGyroscopeMeanFreqXYZ
fBodyAccMag-mean() | FrequencyBodyAccelerometerMagnitudeMean
fBodyAccMag-std() | FrequencyBodyAccelerometerMagnitudeStandardDeviation
fBodyAccMag-meanFreq() | FrequencyBodyAccelerometerMagnitudeMeanFreq
fBodyAccJerkMag-mean() | FrequencyBodyAccelerometerJerkMagnitudeMean
fBodyAccJerkMag-std() | FrequencyBodyAccelerometerJerkMagnitudeStandardDeviation
fBodyAccJerkMag-meanFreq() | FrequencyBodyAccelerometerJerkMagnitudeMeanFreq
fBodyGyroMag-mean() | FrequencyBodyGyroscopeMagnitudeMean
fBodyGyroMag-std() | FrequencyBodyGyroscopeMagnitudeStandardDeviation
fBodyGyroMag-meanFreq() | FrequencyBodyGyroscopeMagnitudeMeanFreq
fBodyGyroJerkMag-mean() | FrequencyBodyGyroscopeJerkMagnitudeMean
fBodyGyroJerkMag-std() | FrequencyBodyGyroscopeJerkMagnitudeStandardDeviation
fBodyGyroJerkMag-meanFreq() | FrequencyBodyGyroscopeJerkMagnitudeMeanFreq

## Detailed Variable Summaries
Variable Name | Variable Summary
------------ | -------------
   Subject | Min.   : 1.0  <br>1st Qu.: 8.0  <br>Median :15.5  <br>Mean   :15.5  <br>3rd Qu.:23.0  <br>Max.   :30.0  
  Activity | Length:180        <br>Class :character  <br>Mode  :character  <br>NA<br>NA<br>NA
TimeBodyAccelerometerMeanX | Min.   :0.2216  <br>1st Qu.:0.2712  <br>Median :0.2770  <br>Mean   :0.2743  <br>3rd Qu.:0.2800  <br>Max.   :0.3015  
TimeBodyAccelerometerMeanY | Min.   :-0.040514  <br>1st Qu.:-0.020022  <br>Median :-0.017262  <br>Mean   :-0.017876  <br>3rd Qu.:-0.014936  <br>Max.   :-0.001308  
TimeBodyAccelerometerMeanZ | Min.   :-0.15251  <br>1st Qu.:-0.11207  <br>Median :-0.10819  <br>Mean   :-0.10916  <br>3rd Qu.:-0.10443  <br>Max.   :-0.07538  
TimeBodyAccelerometerStandardDeviationX | Min.   :-0.9961  <br>1st Qu.:-0.9799  <br>Median :-0.7526  <br>Mean   :-0.5577  <br>3rd Qu.:-0.1984  <br>Max.   : 0.6269  
TimeBodyAccelerometerStandardDeviationY | Min.   :-0.99024  <br>1st Qu.:-0.94205  <br>Median :-0.50897  <br>Mean   :-0.46046  <br>3rd Qu.:-0.03077  <br>Max.   : 0.61694  
TimeBodyAccelerometerStandardDeviationZ | Min.   :-0.9877  <br>1st Qu.:-0.9498  <br>Median :-0.6518  <br>Mean   :-0.5756  <br>3rd Qu.:-0.2306  <br>Max.   : 0.6090  
TimeGravityAccelerometerMeanX | Min.   :-0.6800  <br>1st Qu.: 0.8376  <br>Median : 0.9208  <br>Mean   : 0.6975  <br>3rd Qu.: 0.9425  <br>Max.   : 0.9745  
TimeGravityAccelerometerMeanY | Min.   :-0.47989  <br>1st Qu.:-0.23319  <br>Median :-0.12782  <br>Mean   :-0.01621  <br>3rd Qu.: 0.08773  <br>Max.   : 0.95659  
TimeGravityAccelerometerMeanZ | Min.   :-0.49509  <br>1st Qu.:-0.11726  <br>Median : 0.02384  <br>Mean   : 0.07413  <br>3rd Qu.: 0.14946  <br>Max.   : 0.95787  
TimeGravityAccelerometerStandardDeviationX | Min.   :-0.9968  <br>1st Qu.:-0.9825  <br>Median :-0.9695  <br>Mean   :-0.9638  <br>3rd Qu.:-0.9509  <br>Max.   :-0.8296  
TimeGravityAccelerometerStandardDeviationY | Min.   :-0.9942  <br>1st Qu.:-0.9711  <br>Median :-0.9590  <br>Mean   :-0.9524  <br>3rd Qu.:-0.9370  <br>Max.   :-0.6436  
TimeGravityAccelerometerStandardDeviationZ | Min.   :-0.9910  <br>1st Qu.:-0.9605  <br>Median :-0.9450  <br>Mean   :-0.9364  <br>3rd Qu.:-0.9180  <br>Max.   :-0.6102  
TimeBodyAccelerometerJerkMeanX | Min.   :0.04269  <br>1st Qu.:0.07396  <br>Median :0.07640  <br>Mean   :0.07947  <br>3rd Qu.:0.08330  <br>Max.   :0.13019  
TimeBodyAccelerometerJerkMeanY | Min.   :-0.0386872  <br>1st Qu.: 0.0004664  <br>Median : 0.0094698  <br>Mean   : 0.0075652  <br>3rd Qu.: 0.0134008  <br>Max.   : 0.0568186  
TimeBodyAccelerometerJerkMeanZ | Min.   :-0.067458  <br>1st Qu.:-0.010601  <br>Median :-0.003861  <br>Mean   :-0.004953  <br>3rd Qu.: 0.001958  <br>Max.   : 0.038053  
TimeBodyAccelerometerJerkStandardDeviationX | Min.   :-0.9946  <br>1st Qu.:-0.9832  <br>Median :-0.8104  <br>Mean   :-0.5949  <br>3rd Qu.:-0.2233  <br>Max.   : 0.5443  
TimeBodyAccelerometerJerkStandardDeviationY | Min.   :-0.9895  <br>1st Qu.:-0.9724  <br>Median :-0.7756  <br>Mean   :-0.5654  <br>3rd Qu.:-0.1483  <br>Max.   : 0.3553  
TimeBodyAccelerometerJerkStandardDeviationZ | Min.   :-0.99329  <br>1st Qu.:-0.98266  <br>Median :-0.88366  <br>Mean   :-0.73596  <br>3rd Qu.:-0.51212  <br>Max.   : 0.03102  
TimeBodyGyroscopeMeanX | Min.   :-0.20578  <br>1st Qu.:-0.04712  <br>Median :-0.02871  <br>Mean   :-0.03244  <br>3rd Qu.:-0.01676  <br>Max.   : 0.19270  
TimeBodyGyroscopeMeanY | Min.   :-0.20421  <br>1st Qu.:-0.08955  <br>Median :-0.07318  <br>Mean   :-0.07426  <br>3rd Qu.:-0.06113  <br>Max.   : 0.02747  
TimeBodyGyroscopeMeanZ | Min.   :-0.07245  <br>1st Qu.: 0.07475  <br>Median : 0.08512  <br>Mean   : 0.08744  <br>3rd Qu.: 0.10177  <br>Max.   : 0.17910  
TimeBodyGyroscopeStandardDeviationX | Min.   :-0.9943  <br>1st Qu.:-0.9735  <br>Median :-0.7890  <br>Mean   :-0.6916  <br>3rd Qu.:-0.4414  <br>Max.   : 0.2677  
TimeBodyGyroscopeStandardDeviationY | Min.   :-0.9942  <br>1st Qu.:-0.9629  <br>Median :-0.8017  <br>Mean   :-0.6533  <br>3rd Qu.:-0.4196  <br>Max.   : 0.4765  
TimeBodyGyroscopeStandardDeviationZ | Min.   :-0.9855  <br>1st Qu.:-0.9609  <br>Median :-0.8010  <br>Mean   :-0.6164  <br>3rd Qu.:-0.3106  <br>Max.   : 0.5649  
TimeBodyGyroscopeJerkMeanX | Min.   :-0.15721  <br>1st Qu.:-0.10322  <br>Median :-0.09868  <br>Mean   :-0.09606  <br>3rd Qu.:-0.09110  <br>Max.   :-0.02209  
TimeBodyGyroscopeJerkMeanY | Min.   :-0.07681  <br>1st Qu.:-0.04552  <br>Median :-0.04112  <br>Mean   :-0.04269  <br>3rd Qu.:-0.03842  <br>Max.   :-0.01320  
TimeBodyGyroscopeJerkMeanZ | Min.   :-0.092500  <br>1st Qu.:-0.061725  <br>Median :-0.053430  <br>Mean   :-0.054802  <br>3rd Qu.:-0.048985  <br>Max.   :-0.006941  
TimeBodyGyroscopeJerkStandardDeviationX | Min.   :-0.9965  <br>1st Qu.:-0.9800  <br>Median :-0.8396  <br>Mean   :-0.7036  <br>3rd Qu.:-0.4629  <br>Max.   : 0.1791  
TimeBodyGyroscopeJerkStandardDeviationY | Min.   :-0.9971  <br>1st Qu.:-0.9832  <br>Median :-0.8942  <br>Mean   :-0.7636  <br>3rd Qu.:-0.5861  <br>Max.   : 0.2959  
TimeBodyGyroscopeJerkStandardDeviationZ | Min.   :-0.9954  <br>1st Qu.:-0.9848  <br>Median :-0.8610  <br>Mean   :-0.7096  <br>3rd Qu.:-0.4741  <br>Max.   : 0.1932  
TimeBodyAccelerometerMagnitudeMean | Min.   :-0.9865  <br>1st Qu.:-0.9573  <br>Median :-0.4829  <br>Mean   :-0.4973  <br>3rd Qu.:-0.0919  <br>Max.   : 0.6446  
TimeBodyAccelerometerMagnitudeStandardDeviation | Min.   :-0.9865  <br>1st Qu.:-0.9430  <br>Median :-0.6074  <br>Mean   :-0.5439  <br>3rd Qu.:-0.2090  <br>Max.   : 0.4284  
TimeGravityAccelerometerMagnitudeMean | Min.   :-0.9865  <br>1st Qu.:-0.9573  <br>Median :-0.4829  <br>Mean   :-0.4973  <br>3rd Qu.:-0.0919  <br>Max.   : 0.6446  
TimeGravityAccelerometerMagnitudeStandardDeviation | Min.   :-0.9865  <br>1st Qu.:-0.9430  <br>Median :-0.6074  <br>Mean   :-0.5439  <br>3rd Qu.:-0.2090  <br>Max.   : 0.4284  
TimeBodyAccelerometerJerkMagnitudeMean | Min.   :-0.9928  <br>1st Qu.:-0.9807  <br>Median :-0.8168  <br>Mean   :-0.6079  <br>3rd Qu.:-0.2456  <br>Max.   : 0.4345  
TimeBodyAccelerometerJerkMagnitudeStandardDeviation | Min.   :-0.9946  <br>1st Qu.:-0.9765  <br>Median :-0.8014  <br>Mean   :-0.5842  <br>3rd Qu.:-0.2173  <br>Max.   : 0.4506  
TimeBodyGyroscopeMagnitudeMean | Min.   :-0.9807  <br>1st Qu.:-0.9461  <br>Median :-0.6551  <br>Mean   :-0.5652  <br>3rd Qu.:-0.2159  <br>Max.   : 0.4180  
TimeBodyGyroscopeMagnitudeStandardDeviation | Min.   :-0.9814  <br>1st Qu.:-0.9476  <br>Median :-0.7420  <br>Mean   :-0.6304  <br>3rd Qu.:-0.3602  <br>Max.   : 0.3000  
TimeBodyGyroscopeJerkMagnitudeMean | Min.   :-0.99732  <br>1st Qu.:-0.98515  <br>Median :-0.86479  <br>Mean   :-0.73637  <br>3rd Qu.:-0.51186  <br>Max.   : 0.08758  
TimeBodyGyroscopeJerkMagnitudeStandardDeviation | Min.   :-0.9977  <br>1st Qu.:-0.9805  <br>Median :-0.8809  <br>Mean   :-0.7550  <br>3rd Qu.:-0.5767  <br>Max.   : 0.2502  
FrequencyBodyAccelerometerMeanX | Min.   :-0.9952  <br>1st Qu.:-0.9787  <br>Median :-0.7691  <br>Mean   :-0.5758  <br>3rd Qu.:-0.2174  <br>Max.   : 0.5370  
FrequencyBodyAccelerometerMeanY | Min.   :-0.98903  <br>1st Qu.:-0.95361  <br>Median :-0.59498  <br>Mean   :-0.48873  <br>3rd Qu.:-0.06341  <br>Max.   : 0.52419  
FrequencyBodyAccelerometerMeanZ | Min.   :-0.9895  <br>1st Qu.:-0.9619  <br>Median :-0.7236  <br>Mean   :-0.6297  <br>3rd Qu.:-0.3183  <br>Max.   : 0.2807  
FrequencyBodyAccelerometerStandardDeviationX | Min.   :-0.9966  <br>1st Qu.:-0.9820  <br>Median :-0.7470  <br>Mean   :-0.5522  <br>3rd Qu.:-0.1966  <br>Max.   : 0.6585  
FrequencyBodyAccelerometerStandardDeviationY | Min.   :-0.99068  <br>1st Qu.:-0.94042  <br>Median :-0.51338  <br>Mean   :-0.48148  <br>3rd Qu.:-0.07913  <br>Max.   : 0.56019  
FrequencyBodyAccelerometerStandardDeviationZ | Min.   :-0.9872  <br>1st Qu.:-0.9459  <br>Median :-0.6441  <br>Mean   :-0.5824  <br>3rd Qu.:-0.2655  <br>Max.   : 0.6871  
FrequencyBodyAccelerometerMeanFreqX | Min.   :-0.63591  <br>1st Qu.:-0.39165  <br>Median :-0.25731  <br>Mean   :-0.23227  <br>3rd Qu.:-0.06105  <br>Max.   : 0.15912  
FrequencyBodyAccelerometerMeanFreqY | Min.   :-0.379518  <br>1st Qu.:-0.081314  <br>Median : 0.007855  <br>Mean   : 0.011529  <br>3rd Qu.: 0.086281  <br>Max.   : 0.466528  
FrequencyBodyAccelerometerMeanFreqZ | Min.   :-0.52011  <br>1st Qu.:-0.03629  <br>Median : 0.06582  <br>Mean   : 0.04372  <br>3rd Qu.: 0.17542  <br>Max.   : 0.40253  
FrequencyBodyAccelerometerJerkMeanX | Min.   :-0.9946  <br>1st Qu.:-0.9828  <br>Median :-0.8126  <br>Mean   :-0.6139  <br>3rd Qu.:-0.2820  <br>Max.   : 0.4743  
FrequencyBodyAccelerometerJerkMeanY | Min.   :-0.9894  <br>1st Qu.:-0.9725  <br>Median :-0.7817  <br>Mean   :-0.5882  <br>3rd Qu.:-0.1963  <br>Max.   : 0.2767  
FrequencyBodyAccelerometerJerkMeanZ | Min.   :-0.9920  <br>1st Qu.:-0.9796  <br>Median :-0.8707  <br>Mean   :-0.7144  <br>3rd Qu.:-0.4697  <br>Max.   : 0.1578  
FrequencyBodyAccelerometerJerkStandardDeviationX | Min.   :-0.9951  <br>1st Qu.:-0.9847  <br>Median :-0.8254  <br>Mean   :-0.6121  <br>3rd Qu.:-0.2475  <br>Max.   : 0.4768  
FrequencyBodyAccelerometerJerkStandardDeviationY | Min.   :-0.9905  <br>1st Qu.:-0.9737  <br>Median :-0.7852  <br>Mean   :-0.5707  <br>3rd Qu.:-0.1685  <br>Max.   : 0.3498  
FrequencyBodyAccelerometerJerkStandardDeviationZ | Min.   :-0.993108  <br>1st Qu.:-0.983747  <br>Median :-0.895121  <br>Mean   :-0.756489  <br>3rd Qu.:-0.543787  <br>Max.   :-0.006236  
FrequencyBodyAccelerometerJerkMeanFreqX | Min.   :-0.57604  <br>1st Qu.:-0.28966  <br>Median :-0.06091  <br>Mean   :-0.06910  <br>3rd Qu.: 0.17660  <br>Max.   : 0.33145  
FrequencyBodyAccelerometerJerkMeanFreqY | Min.   :-0.60197  <br>1st Qu.:-0.39751  <br>Median :-0.23209  <br>Mean   :-0.22810  <br>3rd Qu.:-0.04721  <br>Max.   : 0.19568  
FrequencyBodyAccelerometerJerkMeanFreqZ | Min.   :-0.62756  <br>1st Qu.:-0.30867  <br>Median :-0.09187  <br>Mean   :-0.13760  <br>3rd Qu.: 0.03858  <br>Max.   : 0.23011  
FrequencyBodyGyroscopeMeanX | Min.   :-0.9931  <br>1st Qu.:-0.9697  <br>Median :-0.7300  <br>Mean   :-0.6367  <br>3rd Qu.:-0.3387  <br>Max.   : 0.4750  
FrequencyBodyGyroscopeMeanY | Min.   :-0.9940  <br>1st Qu.:-0.9700  <br>Median :-0.8141  <br>Mean   :-0.6767  <br>3rd Qu.:-0.4458  <br>Max.   : 0.3288  
FrequencyBodyGyroscopeMeanZ | Min.   :-0.9860  <br>1st Qu.:-0.9624  <br>Median :-0.7909  <br>Mean   :-0.6044  <br>3rd Qu.:-0.2635  <br>Max.   : 0.4924  
FrequencyBodyGyroscopeStandardDeviationX | Min.   :-0.9947  <br>1st Qu.:-0.9750  <br>Median :-0.8086  <br>Mean   :-0.7110  <br>3rd Qu.:-0.4813  <br>Max.   : 0.1966  
FrequencyBodyGyroscopeStandardDeviationY | Min.   :-0.9944  <br>1st Qu.:-0.9602  <br>Median :-0.7964  <br>Mean   :-0.6454  <br>3rd Qu.:-0.4154  <br>Max.   : 0.6462  
FrequencyBodyGyroscopeStandardDeviationZ | Min.   :-0.9867  <br>1st Qu.:-0.9643  <br>Median :-0.8224  <br>Mean   :-0.6577  <br>3rd Qu.:-0.3916  <br>Max.   : 0.5225  
FrequencyBodyGyroscopeMeanFreqX | Min.   :-0.395770  <br>1st Qu.:-0.213363  <br>Median :-0.115527  <br>Mean   :-0.104551  <br>3rd Qu.: 0.002655  <br>Max.   : 0.249209  
FrequencyBodyGyroscopeMeanFreqY | Min.   :-0.66681  <br>1st Qu.:-0.29433  <br>Median :-0.15794  <br>Mean   :-0.16741  <br>3rd Qu.:-0.04269  <br>Max.   : 0.27314  
FrequencyBodyGyroscopeMeanFreqZ | Min.   :-0.50749  <br>1st Qu.:-0.15481  <br>Median :-0.05081  <br>Mean   :-0.05718  <br>3rd Qu.: 0.04152  <br>Max.   : 0.37707  
FrequencyBodyAccelerometerMagnitudeMean | Min.   :-0.9868  <br>1st Qu.:-0.9560  <br>Median :-0.6703  <br>Mean   :-0.5365  <br>3rd Qu.:-0.1622  <br>Max.   : 0.5866  
FrequencyBodyAccelerometerMagnitudeStandardDeviation | Min.   :-0.9876  <br>1st Qu.:-0.9452  <br>Median :-0.6513  <br>Mean   :-0.6210  <br>3rd Qu.:-0.3654  <br>Max.   : 0.1787  
FrequencyBodyAccelerometerMagnitudeMeanFreq | Min.   :-0.31234  <br>1st Qu.:-0.01475  <br>Median : 0.08132  <br>Mean   : 0.07613  <br>3rd Qu.: 0.17436  <br>Max.   : 0.43585  
FrequencyBodyAccelerometerJerkMagnitudeMean | Min.   :-0.9940  <br>1st Qu.:-0.9770  <br>Median :-0.7940  <br>Mean   :-0.5756  <br>3rd Qu.:-0.1872  <br>Max.   : 0.5384  
FrequencyBodyAccelerometerJerkMagnitudeStandardDeviation | Min.   :-0.9944  <br>1st Qu.:-0.9752  <br>Median :-0.8126  <br>Mean   :-0.5992  <br>3rd Qu.:-0.2668  <br>Max.   : 0.3163  
FrequencyBodyAccelerometerJerkMagnitudeMeanFreq | Min.   :-0.12521  <br>1st Qu.: 0.04527  <br>Median : 0.17198  <br>Mean   : 0.16255  <br>3rd Qu.: 0.27593  <br>Max.   : 0.48809  
FrequencyBodyGyroscopeMagnitudeMean | Min.   :-0.9865  <br>1st Qu.:-0.9616  <br>Median :-0.7657  <br>Mean   :-0.6671  <br>3rd Qu.:-0.4087  <br>Max.   : 0.2040  
FrequencyBodyGyroscopeMagnitudeStandardDeviation | Min.   :-0.9815  <br>1st Qu.:-0.9488  <br>Median :-0.7727  <br>Mean   :-0.6723  <br>3rd Qu.:-0.4277  <br>Max.   : 0.2367  
FrequencyBodyGyroscopeMagnitudeMeanFreq | Min.   :-0.45664  <br>1st Qu.:-0.16951  <br>Median :-0.05352  <br>Mean   :-0.03603  <br>3rd Qu.: 0.08228  <br>Max.   : 0.40952  
FrequencyBodyGyroscopeJerkMagnitudeMean | Min.   :-0.9976  <br>1st Qu.:-0.9813  <br>Median :-0.8779  <br>Mean   :-0.7564  <br>3rd Qu.:-0.5831  <br>Max.   : 0.1466  
FrequencyBodyGyroscopeJerkMagnitudeStandardDeviation | Min.   :-0.9976  <br>1st Qu.:-0.9802  <br>Median :-0.8941  <br>Mean   :-0.7715  <br>3rd Qu.:-0.6081  <br>Max.   : 0.2878  
FrequencyBodyGyroscopeJerkMagnitudeMeanFreq | Min.   :-0.18292  <br>1st Qu.: 0.05423  <br>Median : 0.11156  <br>Mean   : 0.12592  <br>3rd Qu.: 0.20805  <br>Max.   : 0.42630  
