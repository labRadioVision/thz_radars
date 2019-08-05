# thz_radars
Database for FMCW THz radars (HR workspace) and sample code for federated learning

The database contains 3 files:

- Data_test_2.mat: dimension 16000 x 512
  Contains 16000 FFT range measurements (512-point FFT of beat signal after DC removal) used for test database with corresponding labels in   label_test_2.mat  

- Data_train_2.mat: dimension 16000 x 512
  Contains 16000 FFT range measurements (512-point FFT of beat signal after DC removal) used for training database with corresponding labels in   lable_train_2.mat

- label_test_2.mat: dimension 16000 x 1
  Contains the true labels for test data (Data_test_2.mat), namely classes (true labels) correspond to integers from 0 to 7: 
  Class 0: human worker at safe distance >3.5m from the radar (safe distance)
  Class 1: human worker at distance (critical) <0.5m from the corresponding radar
  Class 2: human worker at distance (critical) 0.5m - 1m from the corresponding radar
  Class 3: human worker at distance (critical) 1m - 1.5m from the corresponding radar
  Class 4: human worker at distance (critical) 1.5m - 2m from the corresponding radar
  Class 5: human worker at distance (critical) 2m - 2.5m from the corresponding radar
  Class 6: human worker at distance (critical) 2.5m - 3m from the corresponding radar
  Class 7: human worker at distance (critical) 3m - 3.5m from the corresponding radar
  
- label_train_2.mat: dimension 16000 x 1
  Contains the true labels for train data (Data_train_2.mat), namely classes (true labels) correspond to integers from 0 to 7: 
  Class 0: human worker at safe distance >3.5m from the radar (safe distance)
  Class 1: human worker at distance (critical) <0.5m from the corresponding radar
  Class 2: human worker at distance (critical) 0.5m - 1m from the corresponding radar
  Class 3: human worker at distance (critical) 1m - 1.5m from the corresponding radar
  Class 4: human worker at distance (critical) 1.5m - 2m from the corresponding radar
  Class 5: human worker at distance (critical) 2m - 2.5m from the corresponding radar
  Class 6: human worker at distance (critical) 2.5m - 3m from the corresponding radar
  Class 7: human worker at distance (critical) 3m - 3.5m from the corresponding radar  
  
- permut.mat (1 x 16000)
  contains the chosen random permutation for data partition among nodes/device and federated learnig simulation (see python code)
