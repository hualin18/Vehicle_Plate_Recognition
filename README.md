# vehicle_plate_recognition

The final report is the file named report.pdf. Methods, results and some codes help understand algorithms are shown in this report.

Group member: Huachao Lin

The codes is in codes directory. Codes for plate letter classification is in training.ipynb, for step by step plate segmentation is in LPR.ipynb. The recognition for whole plate dataset is shown in recognition.ipynb. CNN model named 'classifier_nor_20.h5'is also saved in this directory.

The goal of this project is to recognize the plate of each photo. The project mainly consists of two parts: plate segmentation and plate letter recognition. The characters in one plate are seperated one by one. The reference for plate images is [1,2] The letters in plates are formed by numbers ‘0-9’ and letters ‘A-Z’, which is 36 categories in total. The model with best accuracy is used to recognize each letter in a plate. The charactersin a plate are combined and compared with the true label to evaluate the plate recognition accuracy. 

The data for train classification model is zipped as data.zip. Other two file is over 100Mb and you can find it through the link below.

The datasource of the vehicle image dataset.

[1] https://github.com/openalpr/benchmarks/tree/master/seg_and_ocr/usimages

[2] https://github.com/openalpr/benchmarks/tree/master/endtoend/us

The plate segmentation is mainly in three steps:

1. Bluring

The original plate photo is as left and image changed to gray scale is as right

![image](../master/plate.png)     ![image](../master/gray.png)

After changing the color to gray scale, a 5*5 matrix is used to blur the image to avoid some shrap pixels.

![image](../master/blur.png)

2. Thresholding and convert image:

Using proper thresholding algorithm, image can be changed to a clear pattern in white and black color.

![image](../master/threshold.png)

3. Contour and segment:

Using proper contour algorithm,segment each characters of plates out.

![image](../master/contour.png)
