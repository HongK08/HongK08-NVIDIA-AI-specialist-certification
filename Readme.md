# NVIDIA-AI-specialist-certification Report

Title: Traffic detection by identifying vehicle traffic and types

#

Opening background information 
  
  Currently, traffic conditions on the roads in the area are identified in real time, and traffic congestion or the risk of accidents is one of the important problems in     
  routing autonomous cars.
  Therefore, through camera recognition and interpretation of the situation of the road or area, the traffic route should be optimized
  Help to enable driving by excluding situations that may restrict driving, such as safety problems
  
#

General description of the current project 

  The project was learned and implemented using V5 from YOLO among deep learning technologies
  The comparison of vehicle types and the total quantity are detected within a certain area of the current two lanes
  Based on this, the information is provided for use as traffic information or vehicle route designation to predict and avoid traffic congestion and help safe driving. 
  This contributes to enhancing the safety and convenience of autonomous vehicles and their infrastructure systems that will increase further.


#

Proposed Idea for Enhancements to the Project 

  1. YoloV5 offers high accuracy and low processing time, enabling real-time data collection and processing. 
  2. The YoloV5 has excellent detection performance and flexibility to identify and track the target vehicle in multiple environments, making it easy to apply additional features and improvements. 
 
#
Value and Significance of this Project 

  In autonomous driving, safety issues play a key role in road safety.
  The improved system through this project reduces traffic congestion through optimization of routes for future autonomous driving
  And it means being prepared or predictable for safety issues.
  In the end, this project contributes to the smart road system through road control and traffic management in the near future and plays an important role in avoiding predicted or identified risks.

  
#

Current Limitations 

  Current limitations may make it difficult to recognize objects due to weather conditions, i.e., uncontrollable variable conditions, and real-time processing requirements and performance improvements should be made after improving data collection conditions

  
#

Literature Review 

  While working on this project, we are investigating other references, related cases, and papers needed to use YOLOv5 and exploring ideas and technical improvements for this project by reviewing the literature on YOLOv5's performance and future developments.

  
#


Image Acquisition Method 

  1. On YouTube, we recorded a live video of the Colorado Mountain College/Grand Avenue Bridge in Glenwood Springs Live Camera 
  2. Re-shooted a different day/time video on the same resource as number 1 

  Colorado Mountain College/Grand Avenue Bridge in Glenwood Springs Live Camera / URL : https://www.youtube.com/watch?v=B0YjuKbVZ5w

Learning Data Extraction and Learning Annotation 

  First of all, the acquired video was processed to about 15 seconds (Using Radeon Graphics Card Control Panel)

  

#
  
#DarkLabel.zip

  I added classes to darklabel.yml 
  
  ![dark using](https://github.com/user-attachments/assets/91efd64d-9f9e-4033-a199-8d43dbccd97a)
  
  And to use classes, I changed the format1 value classes_set value 
    
  ![image](https://github.com/user-attachments/assets/d6f1aaa6-8140-449f-9ba0-d55849d94878)

  Video was divided into frame units using DarkLabel 2.4.   
  
  ![image](https://github.com/user-attachments/assets/f9b38ef5-24eb-478e-a001-a158a63d15bd)

  
  ![image](https://github.com/user-attachments/assets/438de579-e24a-4e21-994d-d2d323656dfb)

  And you can choose the class value you set above


  
  Annotation is now ready
  
  
  ![image](https://github.com/user-attachments/assets/c36015b9-4a0e-4fb6-bfad-c4a7e877f712)
  
  After all the modifications, the video was imported from DarkLabel to Open Video.
  And all frames were processed by annotating each corresponding vehicle object.
  Finally, store the value in the labels folder via GT Save As And the divided frames were saved in the images folder as PNG 
  
  ![image](https://github.com/user-attachments/assets/07b656b1-973f-4966-b53e-8e452cfce835)
#
  DATA_SET_FILE_URL : https://drive.google.com/file/d/1wbaOHMAbdqJZqfA4KZnEwqn2tdFdJRzA/view?usp=sharing
#

Now it's a picture that Google colab is conducting for learning


![image](https://github.com/user-attachments/assets/435bca6b-ed2e-4bbb-8b27-e3b995796e78)

  1. First, unmount Google Drive and CoLab and then proceed again 
  2. Change the directory to the path you want to use 
  3. And check the current route 

Next
  1. Once again, I changed the installation path to yolov5 (for the data set to put in the future) 
  2. Next is the YOLOv5 installation process 
  3. which was installed in the corresponding path through !gitclone https://github.com/ultralytics/yolov5.git 
  4. I changed the path and even set up the required file through %pipe install -qr requirements.txt 
  5. Finally, installation was completed through Pillow==10.3 
#

![image](https://github.com/user-attachments/assets/8223b1fb-03d0-4924-a311-bb7753537813)
  1. Create a directory where the above organized Train data values will enter and receive the subsequent Val values 
  2. And it's the process of creating data for verification 

#

Put the training data in the created directory according to the path

![image](https://github.com/user-attachments/assets/c7a260ee-7540-44c5-b90b-d184cc3a34a3)


And write down all class modifications and paths in the data.Yaml file

![image](https://github.com/user-attachments/assets/907dd114-3868-4c27-9884-0b44b2fe7db6)


And put the data.Yaml and yolov5n.pt files into the installation path of YOLOv5 on Google Drive

![image](https://github.com/user-attachments/assets/a1e573ab-3a90-4cbf-9d91-c37570716b48)

# 

![image](https://github.com/user-attachments/assets/152802cd-3dc1-4b07-8184-a0b40af0c2cf)

All of them checked the status of the data set after debugging, and all values were confirmed as normal


#
Getting Started with Learning [

![image](https://github.com/user-attachments/assets/20f7b213-6a13-40a3-a5e6-628fa9069c5f)

  1. I imported all the basic libraries 
  2. Check the route
  3. It pre-processes the image files in the directory collectively and stores them in the form of a NumPy array. The preprocessing process includes image resizing and central cutting, and converts the image to the ImageNet standard. The finally generated NumPy array is stored in a form that can be used for deep learning model training.
  4. It is intended to import and resize images to fit the transformation model to 512*512,  Create and store the NumPy array and store it as an npy-type dataset 
  5.  I learned how to learn models with 320 points 

  ![image](https://github.com/user-attachments/assets/1507a437-feeb-4902-98ef-ab56c78ede41)
 
# Model Learning Verification

![confusion_matrix](https://github.com/user-attachments/assets/c5d44430-08cf-416a-9760-aca30d9a7a0e)
![labels](https://github.com/user-attachments/assets/00686531-39b1-45a1-8547-5214dbd40521)


# F1_curve
![F1_curve](https://github.com/user-attachments/assets/dd8c35b3-b377-4ae2-9ec5-b56d786047c5)

#

# P_curve
![P_curve](https://github.com/user-attachments/assets/481fdec5-e2c6-400d-bceb-6efbca58309e)

#

# R_curve
![R_curve](https://github.com/user-attachments/assets/637b1bc0-3d9b-4e9b-a893-359938b0636e)

#

# PR_curve
![PR_curve](https://github.com/user-attachments/assets/cf19fe26-ebf7-4352-aea4-4d8fbe98c4e9)

#

# results
![results](https://github.com/user-attachments/assets/f15451a9-00b4-4026-bf03-928c0501a8ae)

#

# train_batch
![train_batch2](https://github.com/user-attachments/assets/78278814-6746-4cc3-922e-ba017b568c6b)

#

# var_batch
![val_batch2_pred](https://github.com/user-attachments/assets/c1220a16-995c-4660-ad9f-0d8015a7b2b2)

#

# EXP
 https://drive.google.com/file/d/1aGTsXVQlo1TelaWHs35tcel9chyNY8jd/view?usp=sharing
#

And first of all, I tried to run it as a video before marking in the original learning video.

before
https://drive.google.com/file/d/1tv8ih1-WvoEzUrd5Dv_yY59ltg5aHibQ/view?usp=sharing

![image](https://github.com/user-attachments/assets/f2b1bdbc-f711-4050-ba79-60b2b57944c7)
![image](https://github.com/user-attachments/assets/f5eb97b4-7a83-448b-966e-11c863f4f254)


The link to the Google Drive below is the execution result video



https://drive.google.com/file/d/1whYd_78mbLC7Dg0SXT6VijqUsCzR-wFs/view?usp=sharing

Now, we will verify with files with different recording dates/recording times in the same location  



![image](https://github.com/user-attachments/assets/7924b1cc-5e67-480d-92b9-fb54710203ad)
![image](https://github.com/user-attachments/assets/279f4d79-e327-4eda-862b-e0d194821cd7)

#

![image](https://github.com/user-attachments/assets/8b1807ad-86f0-4c9d-8938-22505e973b84)
![image](https://github.com/user-attachments/assets/1f4a0549-e8b5-4bbc-a8d9-1240eab50890)

before
https://drive.google.com/file/d/1tAD-ZZ--VdEnK283c1aICkS0_iKZejb9/view?usp=sharing

This is a file video with a different recording date/recording time in the same place




https://github.com/user-attachments/assets/84c89545-841a-4513-ad81-d2c43a641c14



#
# Full File Link
https://drive.google.com/drive/folders/1FHtsEC5C13EagPtQPVoX3G-u_tUi4maO?usp=sharing




