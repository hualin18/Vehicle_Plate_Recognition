# vehicle_plate_recognition

The final report is shown as report.pdf.

The codes for plate letter recognition is in training.ipynb, step by step plate segmentation is in LPR.ipynb. The regoniation for a plate dataset is shown in main.ipynb. 

The goal of this project is to recognize the plate of each photo in a precise and quick way. The dataset is 300 photos of cars with license plates[1]. The plate's  location is given by x,y coordinates, length and  width of the plate in each corresponding txt file. The photos are taken from different angles and at different distances. The resolution of plates is different from each other as a consequence. The project mainly consists of two parts: plate segmentation and plate letter recognition. Contour algorithm is used for segmentation together with some constraints. The letters in plates are formed by numbers ‘0-9’ and letters ‘A-Z’, which is 36 categories in total. Random forest, neural network and etc methods are used to build single letter recognition model with a dataset[2] of 36576 28*28 standard images of 36 categories. The model with best accuracy is used to recognize each letter in a plate and the letters in a plate are compared with the true label to evaluate the plate recognition accuracy. 


The datasource of the dataset.
[1]
[2]
