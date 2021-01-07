## project discription:
The code is used to evaluate characteristic values in temperature profiles taken with a thermal camera during an inline process monitoring step of a moving object. 
During the measurement the object of interest (here the high temperature peak in the profile) is chaning the incoming direction into the measured image.  
The code is designed to extract specific information from the temperature profil for research aims. As the speed of the calculation was not of interest, the code is not designed to the highest standards.

## proceedure:
### 1st step:
To extract the needed temperature profile from the measured data, the Python library flirpy (DOI 10.5281/zenodo.3866331) is used to convert the data optained by an FLIR thermal camera into a processable format.

### 2nd step:
First the variables for the calculation are defined. The determination is empirical and will be needed to be adapted to your specific task. It is recommended to itteratively optimise those values to achieve the best results.

### 3rd step:
Start the calculation of the specific values from the temperature profile. Therefore, each frame of the given data set is individually considered and the values are determined.
Firstly, the code reads the information provided in the excel sheet "Ablagepunkt". If your folder structur has different levels (here up to three) the excel sheet "Ablagepunkt" on the high level will be considered.
In the excel sheet four values (x1, y1, x2, y2), describing the straight line along which the temperature profile will be obtained, can be given. This staight line can be an horizontal line at a certain y-pixel (as e.g. the default value) or a diagonale line through the image. 
To get a good impression of the temperature profiles an image of the obtained profile is printed. In case the incoming direction of the observed, warm object is changed and therefore the images are flipped in the following, a defined number (here 15) of those single images is recalculated.
After every single image is considered a excel sheet with all the characteristic values is created and can be used for further culculations.
An overview about the proceedure and the definition of some of the characteristic is graphically shown in the image "Characteristics_image.jpg", which can be found in the folder doc.

## test data:
To test the code an exemplary data set is provided in which for an horizontal line three temperature peaks with increasing hights will be seen.



