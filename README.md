# Audio-classifier

* This repository contains Data Visualization, Data Preprocessing, Modeling and finally, Classification of Audio Dataset 
 and comparison of the different Machine Learning Algorithms used. <br>

**Process:** Data Visulaization using Spectrogram, Wave Shape Plotting, Preprocessing using Spectral Centroids, Mean (Average), Minimum and Maximum of Data Points, Modeling and Classification using Extra Tree Classifier, Random Forrest Classifier, Logistic Regression, XGBRegressor and a seperate approach using OpenCV using image file generated from Spectrograms of the Audio files. Several Clustering Algorithms (K-Means, Mean Shift, Gaussian Mixture Model & Agglomerative Clustering) were also used to visualize different clusters.<br><br>

The following files are included in this repository:<br>
    **1.  - For creating proper CSV file to be used as Metadata for Preprocessing and Machine Learning Algorithm.<br><br>
    **2.  - For preprocessing the Audio HDF5 (Hierarchical Data Format) files containing sound texture data (E dB Data, f_tract & s_tract) and PTNE (Pulse, Tone, Noise & Energy) Data. In this the Spectral Centroids of the tract data (E dB Data, f_tract & s_tract) are calculated as well as the Mean (Average), Min and Max are calculated from the PTNE data. The generation of the Tract data and PTNE data are explained in this paper: *https://arxiv.org/abs/1705.05271*.<br><br>
    **3. - For visualizing the Tract and PTNE data where Spectrograms of desired file can be viewed.<br><br>
    **4. - Another visualization tool where the different classes of the data can be viewed as Spectrograms and Wave shapes. Also, an explanation is provided for the motivation behind selecting the features.<br><br>
    **5. - For Modeling Machine Learning Algorithms (Extra Tree Classifier, Random Forrest Classifier, Logistic Regression & XGBRegressor) using the Spectral Centroids from Tract Data (E dB, f_tract and s_tract) and Mean, Min and Max from PTNE Data (Pulse, Tone, Noise and Energy). Classification using the above ML Classifiers, plotting the Confusion Matrix and calculating Accuracies of different Classifiers are also included in the file.<br><br>
    **6. - For clustering using K-Means, Mean Shift, Gaussian Mixture Model and Agglomerative Clustering. The data is just visualized as separate clusters. Since it is unsupervised, no classification is done.<br><br>
    **7. - A second approach is used other than Spectral Centroid method in which the Spectrograms of the Tract data are exported as seperate images (*Dataset_image* folder). The folder will contain separate spectrogram image files for E dB, f_tract and s_tract data.<br><br>
    **8. - A CNN (Convolutional Neural Network) is implemented by processing the spectrogram images saved using the above preprocessing where the images are converted to arrays and then concatenated. The CNN Classifier is trained and tested using the concatenated arrays.<br><br>
    **9. - Validation using the CNN Classifier. The Prediction Algorithm processes the spectrogram images saved earlier in the *Dataset_image* folder and predicts the class based on the training.<br><br>

    **Keywords:** Spectrograms, Spectral Centroid, Extra Tree Classifier, Random Forrest Classifier, Logistic Regression, XGBRegressor, Clustering, K-Means, Mean Shift, Gaussian Mixture Model, Agglomerative Clustering, CNN, OpenCV. <br>
    
<!-- **Note 1:** Accuracies of all algorithms used is this repository are displayed in the Modeling & Classification files (*5_AED_C_clasification_modeling_SC_v1.ipynb & 8_AED_C_clasification_modeling_opencv_v1.ipynb*).<br><br>
**Note 2:** The Metadata CSV files a very important role in all of the above files as the catagories are defined in the CSV file. And the CSV files is the first file that is loaded into all the above methods.<br><br>
**Note 3:** Due to storage size limitation of GitHub, the Dataset HDF5 files from the *ESC_50_Subset* were not uploaded. Instead the *npy files (ptne_features.npy & spectrum_features.npy)* generated by the preprocessing the HDF5 files are included in the repository to be used for Modeling and Classification using the Spectral Centroid Method (*5_AED_C_clasification_modeling_SC_v1.ipynb*). The Spectrogram images generated by the OpenCV Preprocessing (*7_AED_C_preprocessing_opencv_v1.ipynb*) are also inlcuded in the repository (in the *Dataset_image* folder) to be used for the CNN method (*8_AED_C_clasification_modeling_opencv_v1.ipynb & 9_AED_C_prediction_opencv_v1.ipynb*). -->
