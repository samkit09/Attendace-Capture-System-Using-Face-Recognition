# ATTENDANCE CAPTURING SYSTEM USING FACE RECOGNITION

![image](https://user-images.githubusercontent.com/64376922/120899558-eadc0000-c64d-11eb-9056-d77e2b37e865.png)

## INTRODUCTION
The main purpose of making this project is to help teachers all around the globe to perform a task that might seem easy at first but will get more and more frustrating over time. This task of taking attendance can be made convenient by implementing our machine learning model implemented with our user interface.
The ACS is a web portal. All datasets for the ACS are modified using driver programs. These programs include face creation, face detection, face recognition and other such models.

#### Hardware Interface
This system is deployed on a webpage using flask and html. There are 2 interfaces, one for the student which takes the students face video as an input and the other web page for the teachers to input their class photos and get the attendance as a result in table format. They can also download the attendance.

#### Software Interfaces
In this system, we maintain two drivers. These drivers include face creation (driver 1) and attendance capturing (driver 2). The student’s face information is processed by the driver 1 and the model is trained accordingly after which we can capture attendance.

#### Project Functions
- Allows student to input face to train model for taking attendance.
- Allows teacher to input class photo to capture attendance easily.
- Creates an attendance report for teacher to see which student is present and which is absent.
- It allows the teacher to download the excel file of the attendance report to add it in their records.
- Ease of use and efficient attendance capturing for the teachers’ conveniences.

## DESCRIPTION
#### User Classes and Characteristics
1. Teacher
- The teacher will input class photo to capture attendance easily.
- Then model creates an attendance report for teacher to see which student is present and which is absent.
- Model allows the teacher to download the excel file of the attendance report to add it in their records.

2. Student
- The student will put their face video as an input. The longer the video more the photos it will take for training the model. We recommend taking a 20 second video.

#### Working
1.	User provides their face video (minimum 20 seconds) named with their names and roll numbers through the front-end interface provided that will be stored in the directory.
2.	Driver Code 1:
    - After all users provided their videos, faces will be detected and saved in individual directories (Train, Val) with their names. 
    -	Images are converted to arrays and stored.
    -	Embeddings are created from these images which are stored as well.
    -	SVM classifier model is trained and saved.
3.	Driver 2: 
    -	Class photo is taken as input.
    -	Faces will be detected and saved in another directory. 
    -	Images are converted to arrays.
    -	Embeddings are created from these images.
    -	Face Recognition is performed on detected faces.
    -	Names of the recognized faces are added to the attendance report as present or 1 while the other faces are marked as absent or 0.
    -	This report is then displayed on the frontend.
    -	A download button is also provided for the report.
 
#### Workflow
The diagram given below displays the actual working of our project involving every aspect of the program in brief:

![image](https://user-images.githubusercontent.com/64376922/120899421-4bb70880-c64d-11eb-9a89-eb0c8afe0f6d.png)

## COMPONENTS
#### Video to be submitted: (Video_Upload.ipynb)
![image](https://user-images.githubusercontent.com/64376922/120899311-b61b7900-c64c-11eb-879f-09526d9a3f13.png)

#### Video Submitted: (Video_Upload.ipynb)
![image](https://user-images.githubusercontent.com/64376922/120899322-c6cbef00-c64c-11eb-9e0d-6ffa042cfb07.png)

#### Final Output Report: (Trainer_Code.ipynb)
The “Train Model” button executes driver_code1.ipynb (to be executed only once) while the “Check” button executes driver_code2.ipynb.

![image](https://user-images.githubusercontent.com/64376922/120899353-f3800680-c64c-11eb-82ed-3621dfdd4525.png)

## CONCLUSION
The project made will help all the teachers worldwide, will display efficiency in the education sector. The ease of just uploading the class photo on a website and receiving instant attendance report would prove useful for teachers in a hurry. The future scope of this project is very large. An SQL server can be used to send attendance to the college database and that would lessen even this task of teachers taking attendance. We hope that with our project several schools would take this at use and implement it in their systems.
