Handwriting-Recognition
=======================

A prototype for offline recognition of handwritten (cursive) words using holistic features.

The implemented system exists as several image feature extraction prototype functions developed using MATLAB. The Image Processing Toolkit is essential for the correct execution of the system. http://uk.mathworks.com/products/image/

Some knowledge of pattern recognition or digital image processing may be beneficial, but is not required. Where necessary, code commentary will attempt to clarify the purpose of specific code regions.

It is recommend that the user execute the feature extraction functions prior to executing the classification function. In doing so the user should gain an understanding of the specific image features extracted.

The file 'nFoldAll.m' can be considered as a test harness which calls the feature extraction prototypes and provides classifier functionality.


Feature Extraction Prototypes 
=============================
Name: protoCentroid.m 
Inputs: Image Filename, display argument, stats argument 
Outputs: Centroid co-ords, eccentricity measurement, No. connected components 

Name: protoCrossing.m  
Inputs: Image Filename, display argument, stats argument
Outputs: No. Foreground pixels 

Name: protoChain.m Image 
Inputs: Filename 
Outputs: Normalised FCC, No. connected components  

Name: protoEuler.m Image 
Inputs: Filename 
Outputs: Euler No., No. connected components 

Name: protoHDensity.m
Inputs: Image Filename, display argument, stats argument
Outputs: Normalised densities

Name: protoVDensity.m
Inputs: Image Filename, display argument, stats argument
Outputs: Normalised densities,  upper %, lower %  

Classification Prototype  
=========================
Name:  nFoldAll.m
Inputs: Integer  1 - 10: Specifies training/testing set configuration
Outputs: ASCII List: List of ASCII transcriptions of word images    

Supporting Functions
=======================
Fchcode.m - Gonzalez (2004) 
Boundaries.m - Gonzalez (2004) 
Knnclassify - http://uk.mathworks.com/help/bioinfo/ref/knnclassify.html

Dataset
========

Dataset of images provided consists of the top 30 most frequently occuring words in the University of Bern IAM v2.0 database.

IAM Handwriting Database http://www.iam.unibe.ch/fki/databases/iam-handwriting-database

U. Marti and H. Bunke. The IAM-database: An English Sentence Database for Off-line Handwriting Recognition. Int'l Journal on Document Analysis and Recognition, Volume 5, pages 39 - 46, 2002.
