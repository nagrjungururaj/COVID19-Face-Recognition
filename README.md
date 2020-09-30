# Face-Recognition-pandemic-special
Face Recognition Algorithm for masked and unmasked faces with high accuracy
## About
Algorithm uses a pre-trained models provided by Intel Openvino Platform. It has 3 steps:  
a) Face detector detects single or multiple faces  
b) The cropped faces are passed as input to landmarks-regressor model which calculates 5 landmarks of detected faces and matches with the training database using regression  
c) Using the detected face and keypoints the face recognizer model matches the detected face with the exisiting face in the train database and produces a matching cosine distance which decides the face id  
## Installing Openvino
For Windows : https://docs.openvinotoolkit.org/latest/openvino_docs_install_guides_installing_openvino_windows.html  
For Linux/Ubuntu : https://docs.openvinotoolkit.org/latest/openvino_docs_install_guides_installing_openvino_linux.html  
## Essentials : 
1. pip install requirements.txt  
2. Activate openvino (Without this the code wont run !)  
   a) Windows 10 : Go to command prompt and paste : C:\Program Files(x86)\IntelSWTools\openvino\bin\setupvars.bat  
   b) Linux/Ubuntu : Run export PYTHONPATH="$/opt/intel/openvino/python/python3:$PYTHONPATH" and Run source $HOME/.bashrc 
## Steps :
1. Prepare the masked data using the link https://github.com/prajnasb/observations/tree/master/mask_classifier/Data_Generator
2. Prepare the unmasked data using the link https://docs.openvinotoolkit.org/2020.1/_demos_python_demos_face_recognition_demo_README.html
3. Combine the pictures for masked images and unmasked images and copy to face_gallery folder
4. Run face_recognition_demo.py
