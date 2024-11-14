# NVIDIA-AI-specialist-certification Report

Title: Traffic detection by identifying vehicle traffic and types

주제 : 차량 통행과 종류 파악을 통한 교통량 감지
#

Opening background information [배경 정보]
  
  Currently, traffic conditions on the roads in the area are identified in real time, and traffic congestion or the risk of accidents is one of the important problems in     
  routing autonomous cars.
  Therefore, through camera recognition and interpretation of the situation of the road or area, the traffic route should be optimized
  Help to enable driving by excluding situations that may restrict driving, such as safety problems

  현재 해당 지역 도로의 교통상황을 실시간으로 파악하여 교통 체증의 발생 또는 사고의 발생 위험 등은 자율주행 자동차의 경로 지정에 있어서 중요한 문제 중 하나입니다.
  그래서 해당 도로 또는 구역의 상황을 카메라로 인식과 해석을 통하여 교통 경로의 최적화와 안전 문제 등 운행에 제한이 될 수 있는 상황을 배제하고 주행이 가능하도록 돕는다
  
#

General description of the current project [프로젝트 전반적 설명]

  The project was learned and implemented using V5 from YOLO among deep learning technologies
  The comparison of vehicle types and the total quantity are detected within a certain area of the current two lanes
  Based on this, the information is provided for use as traffic information or vehicle route designation to predict and avoid traffic congestion and help safe driving. 
  This contributes to enhancing the safety and convenience of autonomous vehicles and their infrastructure systems that will increase further.

  이 프로젝트는 딥 러닝 기술 중 YOLO의 V5를 사용하여 학습 및 구현되었습니다
  차량 유형 및 총량 비교는 현재 두 차선의 특정 영역 내에서 감지됩니다
  이를 바탕으로 교통 혼잡을 예측하고 피하고 안전 운전을 돕기 위한 교통 정보 또는 차량 경로 지정으로 사용할 수 있도록 정보를 제공합니다.
  이는 앞으로 더욱 증가할 자율주행차 및 인프라 시스템의 안전과 편의성을 강화하는 데 기여할 것입니다.
  
#

Proposed Idea for Enhancements to the Project [제안하고 싶은 프로젝트의 강점]

  1. YoloV5 offers high accuracy and low processing time, enabling real-time data collection and processing. [YoloV5는 높은 정확도와 낮은 처리 시간을 제공하여 Real-Time 방식의 데이터 수집과 처리를 가능하게 합니다.]
  2. The YoloV5 has excellent detection performance and flexibility to identify and track the target vehicle in multiple environments, making it easy to apply additional features and improvements. [YoloV5는 여러 환경에서 대상 차량을 식별하고 추적할 수 있는 뛰어난 감지성능과 유연성을 가지며, 추가적인 기능과 개선 사항을 쉽게 적용이 가능합니다.]
 
#
Value and Significance of this Project [프로젝트 가치와 중요성]

  In autonomous driving, safety issues play a key role in road safety.
  The improved system through this project reduces traffic congestion through optimization of routes for future autonomous driving
  And it means being prepared or predictable for safety issues.
  In the end, this project contributes to the smart road system through road control and traffic management in the near future and plays an important role in avoiding predicted or identified risks.

  자율 주행 에서는 안전 문제가 도로 안전에 핵심으로 작용한다. 
  이 프로젝트를 통해 개선 된 시스템은 앞으로의 자율 주행에 있어 경로의 최적화를 통한 교통체증의 감소
  그리고 안전 문제에 있어서 미리 대비하거나 예측 가능하게 함을 의미한다.
  결국 이 프로젝트는 앞으로 다가올 가까운 미래나 그 이후에서도 도로 통제 그리고 교통 관리 등으로 스마트 도로 시스템에 기여하며 예측하거나 파악한 위험을 회피하는데 중요한 역할을 한다.
  
#

Current Limitations [직면하고 있는 한계]

  Current limitations may make it difficult to recognize objects due to weather conditions, i.e., uncontrollable variable conditions, and real-time processing requirements and performance improvements should be made after improving data collection conditions

  현재의 한계로는 기상 조건 즉 통제 불가능한 변인 조건에 의한 대상의 인식이 어려워 질 수 있으며, 데이터 수집 조건의 개선 이후에 실시간 처리에 대한 요구 사항 그리고 성능 향상이 이루어져야 한다
  
#

Literature Review [문헌 고찰]

  While working on this project, we are investigating other references, related cases, and papers needed to use YOLOv5 and exploring ideas and technical improvements for this project by reviewing the literature on YOLOv5's performance and future developments.

  이 프로젝트를 진행하며 YOLOv5를 사용하는데 있어서 필요한 다른 레퍼런스와 관련 사례 그리고 논문 등을 조사하고 있으며 YOLOv5의 성능과 앞으로의 발전에 대한 문헌을 검토를 통한 이 프로젝트의 아이디어와 기술적인 측면에서의 개선 방안을 탐구하고 있다.
  
#


Image Acquisition Method [영상 취득 방법]

  1. On YouTube, we recorded a live video of the Colorado Mountain College/Grand Avenue Bridge in Glenwood Springs Live Camera [유튜브에서 글렌우드 스프링스의 콜로라도 마운틴 칼리지/그랜드 애비뉴 다리 라이브 카메라 영상을 녹화했습니다.]
  2. Re-shooted a different day/time video on the same resource as number 1 [1번과 동일한 리소스에 다른 날/시간의 영상을 한 번 재 촬영 했습니다.]

  Colorado Mountain College/Grand Avenue Bridge in Glenwood Springs Live Camera / URL : https://www.youtube.com/watch?v=B0YjuKbVZ5w

Learning Data Extraction and Learning Annotation [학습 데이터 추출과 학습 어노테이션]

  First of all, the acquired video was processed to about 15 seconds (Using Radeon Graphics Card Control Panel)

  우선 취득한 영상의 분량을 약 15초 정도로 가공하였습니다 (라데온 그래픽카드 제어판 사용함)

#
  
#DarkLabel.zip

  I added classes to darklabel.yml 
  
  darklabel.yml 에 classes를 추가하였다 
  ![dark using](https://github.com/user-attachments/assets/91efd64d-9f9e-4033-a199-8d43dbccd97a)
  
  And to use classes, I changed the format1 value classes_set value 
  
  그리고 classes를 사용하기 위하여 format1 값 classes_set 값을 변경해주었다 
  ![image](https://github.com/user-attachments/assets/d6f1aaa6-8140-449f-9ba0-d55849d94878)

  Video was divided into frame units using DarkLabel 2.4.   
  
  DarkLabel 2.4 를 사용하여 비디오를 프레임 단위로 분할하였다. 
  ![image](https://github.com/user-attachments/assets/f9b38ef5-24eb-478e-a001-a158a63d15bd)

  
  ![image](https://github.com/user-attachments/assets/438de579-e24a-4e21-994d-d2d323656dfb)

  And you can choose the class value you set above

  
  그리고 위에서 설정한 클래스 값을 선택해 주면 된다
  
  
  Annotation is now ready
  
  이제 Annotation 준비가 완료되었다
  ![image](https://github.com/user-attachments/assets/c36015b9-4a0e-4fb6-bfad-c4a7e877f712)
  
  After all the modifications, the video was imported from DarkLabel to Open Video.
  And all frames were processed by annotating each corresponding vehicle object.
  Finally, store the value in the labels folder via GT Save As And the divided frames were saved in the images folder as PNG 
  
  모든 수정 후 동영상은 DarkLabel에서 Open Video로 가져옵니다.
  그리고 모든 프레임은 해당 차량 객체에 주석을 달아서 처리되었습니다.
  마지막으로 GT 세이브 As를 통해 라벨 폴더에 값을 저장합니다.
  그리고 분할된 프레임은 이미지 폴더에 PNG로 저장되었습니다. 
  ![image](https://github.com/user-attachments/assets/07b656b1-973f-4966-b53e-8e452cfce835)
#
  DATA_SET_FILE_URL : https://drive.google.com/file/d/1wbaOHMAbdqJZqfA4KZnEwqn2tdFdJRzA/view?usp=sharing
#

Now it's a picture that Google colab is conducting for learning

이제 학습을 위해 구글 colab 에서 진행하는 사진이다
![image](https://github.com/user-attachments/assets/435bca6b-ed2e-4bbb-8b27-e3b995796e78)

  1. First, unmount Google Drive and CoLab and then proceed again [먼저 Google 드라이브 및 CoLab 마운트를 해제한 다음 다시 진행합니다]
  2. Change the directory to the path you want to use [사용할 경로로 디렉토리 변경]
  3. And check the current route [그리고 현재 경로 확인]

Next
  1. Once again, I changed the installation path to yolov5 (for the data set to put in the future) [다시한번 설치 경로를 yolov5 으로 바꿔주었다.(앞으로 넣을 데이터 셋을 위함)]
  2. Next is the YOLOv5 installation process [다음으로는  YOLOv5 설치하는 과정]
  3. which was installed in the corresponding path through !gitclone https://github.com/ultralytics/yolov5.git [!git clone https://github.com/ultralytics/yolov5.git 을 통하여 해당 경로에 설치하였고]
  4. I changed the path and even set up the required file through %pipe install -qr requirements.txt [경로를 바꾸고 %pip install -qr requirements.txt 를 통하여 필수 파일까지 설정 완료하였다]
  5. Finally, installation was completed through Pillow==10.3 [마지막으로 Pillow==10.3 을 통하여 설치까지 완료하였음]

     

   

  
  


  
  


  
