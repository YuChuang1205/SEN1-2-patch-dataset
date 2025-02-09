# SEN1-2 patch dataset   

### !!! Note: The complete training and testing code (Integrates multiple networks) can be found in [[Link](https://github.com/YuChuang1205/RRL-Net)]

### A brief introduction to the SEN1-2 patch dataset
SEN1-2 patch dataset is an optical and SAR image patch matching dataset with the patch size of 64 × 64 pixels based on the SEN1-2 dataset [[paper(dataset)](https://www.engineeringvillage.com/app/doc/?docid=cpx_M7ba0a706172513b3723M75c510178163190&pageSize=25&index=2&searchId=f7f4d9d0bf3e488397e590cd9d1aa68c&resultsCount=2&usageZone=resultslist&usageOrigin=searchresults&searchType=Quick)] 
and SIFT keypoint extraction. The dataset contains a total of 800000 pairs of cross-spectral image patches with equal numbers of positive and negative samples. training set : test set=3 : 1 (600000 : 200000).    


### Document interpretation  
1. "finally_train.txt" denotes the point pair information of the training set.   
2. "finally_test.txt" denotes the point pair information of the test set.   
3. Each line in txt denotes a sample pair.   
4. Take one line as an example. The meaning of the corresponding position in "ROIs1970_fall,s1_25,ROIs1970_fall_s1_25_p621.png,81,155,s2_25,ROIs1970_fall_s2_25_p621.png,172,91,0" is 
"The folder name from SEN1-2 patch dataset"; "the sub-folder name of SAR image"; "the image name of SAR image"; "The x-coordinate of the keypoint of the SAR image"; "The y-coordinate of the keypoint of the SAR image" 
"the sub-folder name of optical image"; "the image name of optical image"; "The x-coordinate of the keypoint of the optical image"; "The y-coordinate of the keypoint of the optical image" 
"The label of the image pair. 1 for matching, 0 for nonmatching".    



### Construction of the dataset  
1. Download SEN1-2 dataset [[paper(dataset)](https://www.engineeringvillage.com/app/doc/?docid=cpx_M7ba0a706172513b3723M75c510178163190&pageSize=25&index=2&searchId=f7f4d9d0bf3e488397e590cd9d1aa68c&resultsCount=2&usageZone=resultslist&usageOrigin=searchresults&searchType=Quick)].     
2. Build the corresponding dataset according to the point pair information in "finally_train.txt" and "finally_test.txt".   


### Other supplements
To view the experimental benchmark based on this data set, please view our paper "Feature Interaction Learning Network for Cross-Spectral Image Patch Matching" [[link](https://ieeexplore.ieee.org/document/10251126)] published on *IEEE Transactions on Image Processing*. It is worth noting that the epochs of all methods in this experimental benchmark are set to 40.




   


