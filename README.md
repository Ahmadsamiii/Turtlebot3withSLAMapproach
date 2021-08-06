# Turtlebot3 with SLAM approach

## Steps of Use Turtlebot3 with SLAM approach to create and save a map:


- **Step-1:** PC Setup steps

   1.1 Install Oracle VM VirtualBox from [this link](https://www.virtualbox.org/wiki/Downloads).
            
     ![image](https://user-images.githubusercontent.com/85820553/128093150-99c207d5-3751-4e01-809d-2661c634f070.png)



   1.2 Install Ubuntu 18.04 from [this link](https://releases.ubuntu.com/18.04).
            
   Follow [this video](https://youtu.be/QbmRXJJKsvs) steps to install Ubuntu 18.04 on Oracle VM VirtualBox
   
   
   
   ![image](https://user-images.githubusercontent.com/85820553/128093284-1557b366-e695-40c7-9f92-3767148c40b7.png)
   
   
   
    1.3 Install Install ROS 1 on Remote PC by executing the following next commands:
            
            
   <!-->
         sudo apt install python-rosdep
![image](https://user-images.githubusercontent.com/85820553/128537254-a949b4ab-dbae-46e5-ba6c-6815afd4c8ba.png)



   <!-->
         sudo apt upgrade
         
![image](https://user-images.githubusercontent.com/85820553/128538608-0dd3e21e-1229-4871-961e-e5685343561e.png)


![image](https://user-images.githubusercontent.com/85820553/128538662-d740ea7f-f135-478e-b109-2b061c37d086.png)


![image](https://user-images.githubusercontent.com/85820553/128538700-8667425a-596e-426d-b84c-88fe2339a059.png)



   <!-->
         wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_melodic.sh


![image](https://user-images.githubusercontent.com/85820553/128538814-306c6798-8517-4791-bcb1-43472bc87ffb.png)



   <!-->
         chmod 755 ./install_ros_melodic.sh 
         
         
![image](https://user-images.githubusercontent.com/85820553/128539078-858410b6-8943-4743-be09-4eb3c4057fdb.png)


   <!-->
         bash ./install_ros_melodic.sh


![image](https://user-images.githubusercontent.com/85820553/128544031-2a6df814-54ae-4784-887f-2ac7c88fe05f.png)

sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy \
![image](https://user-images.githubusercontent.com/85820553/128544089-625c3c10-300c-467f-88c6-b77f4e591d5a.png)


![image](https://user-images.githubusercontent.com/85820553/128544108-4c9dd8a9-1b61-46a0-8a58-d7090327e771.png)



  1.4 Install Dependent ROS 1 Packages by executing the following next commands:


   <!-->
         sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy 
         
         
         
  ![image](https://user-images.githubusercontent.com/85820553/128547309-cdee36c9-fd55-4e83-b5d4-65e237a71673.png)
  
  
  
  ![image](https://user-images.githubusercontent.com/85820553/128547348-8a6e95cb-cf31-4986-92e8-8d48dc7e865e.png)
  
  
  
     <!-->
         sudo apt-get install ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc 
         
         
![image](https://user-images.githubusercontent.com/85820553/128547766-f326786d-471a-49c8-b02a-ebcb66a8101f.png)



     <!-->
         sudo apt-get install ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan
         
         
![image](https://user-images.githubusercontent.com/85820553/128547886-69eac8ae-e895-4053-aa8e-126c7ede7c43.png)
  


     <!-->
         sudo apt-get install ros-melodic-rosserial-arduino ros-melodic-rosserial-python
         
![image](https://user-images.githubusercontent.com/85820553/128548013-0f81d390-3b30-48af-b5b0-7a3a139e794b.png)



     <!-->
         sudo apt-get install ros-melodic-rosserial-server ros-melodic-rosserial-client
         
![image](https://user-images.githubusercontent.com/85820553/128548083-131d15a8-af2c-4dd3-91d6-8b03a4d1fba9.png)




     <!-->
         sudo apt-get install ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server
         
![image](https://user-images.githubusercontent.com/85820553/128548443-7f9db29c-4b4b-4065-a210-bd419400053f.png)



![image](https://user-images.githubusercontent.com/85820553/128548464-9ce14cab-cf76-4dd0-99e8-4c73eca55982.png)



![image](https://user-images.githubusercontent.com/85820553/128548969-f62c8649-c09b-4d1f-83b6-d0c2dd80deff.png)



     <!-->
         sudo apt-get install ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro
         
         
![image](https://user-images.githubusercontent.com/85820553/128557380-0bdc2b8b-da67-4704-a574-9a99b221ea76.png)


![image](https://user-images.githubusercontent.com/85820553/128557412-b4e54858-b995-4b09-a0a4-0d2535ef8b5b.png)


![image](https://user-images.githubusercontent.com/85820553/128557432-2e361d2d-86dd-49d0-8845-b45369cbf583.png)




     <!-->
         sudo apt-get install ros-melodic-compressed-image-transport ros-melodic-rqt*
         
         
![image](https://user-images.githubusercontent.com/85820553/128557571-0de072c3-3ade-4d86-99b4-f1988660db55.png)



![image](https://user-images.githubusercontent.com/85820553/128557599-f416dd40-a3bc-46f3-8e27-8b00b43bc3c6.png)



![image](https://user-images.githubusercontent.com/85820553/128557613-e2daf10d-7b33-4af5-85a2-56ed95feecc0.png)




     <!-->
         sudo apt-get install ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers
         
         
![image](https://user-images.githubusercontent.com/85820553/128557730-8891baec-1ab6-438e-812c-22f62d2b44dc.png)


![image](https://user-images.githubusercontent.com/85820553/128557749-b075c049-53c1-483d-8c11-da6e8ecb2f89.png)


![image](https://user-images.githubusercontent.com/85820553/128557765-030e757f-6cae-44cc-a453-cf1a27b21d44.png)




1.5 Install TurtleBot3 Packages by executing the following next commands:



     <!-->
         sudo apt-get install ros-melodic-dynamixel-sdk

![image](https://user-images.githubusercontent.com/85820553/128557994-01771fad-a43c-4a5c-b3b0-a965beef62f5.png)



     <!-->
         sudo apt-get install ros-melodic-turtlebot3-msgs

![image](https://user-images.githubusercontent.com/85820553/128558105-8a981a97-84bb-4eb4-945b-7b43321d2f85.png)


     <!-->
         sudo apt-get install ros-melodic-turtlebot3

![image](https://user-images.githubusercontent.com/85820553/128558249-ca7cc35e-d4da-4ead-b132-34048bbc899b.png)




![image](https://user-images.githubusercontent.com/85820553/128558282-2b35407b-39f5-4862-a9f7-e1ddec287b51.png)




![image](https://user-images.githubusercontent.com/85820553/128558297-8aa36b36-8f0d-40af-9991-6baa97dd056e.png)



         


1.5 Set TurtleBot3 Model Name by executing the following next commands:



In case of TurtleBot3 Burger:
     <!-->
         echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc


![image](https://user-images.githubusercontent.com/85820553/128558445-15befea0-ea1b-4b6f-8cd6-8da614c89994.png)




In case of TurtleBot3 Waffle Pi

     <!-->
         echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc

![image](https://user-images.githubusercontent.com/85820553/128558613-703b80f4-86e8-49f3-a897-2ce146244893.png)




1.6 Network Configuration:


1.6.1 Connect PC to a WiFi device and find the assigned IP address with the command below:


     <!-->
         ifconfig

![image](https://user-images.githubusercontent.com/85820553/128559191-745e86a0-366e-414b-bd05-eca98ebbfbf5.png)



1.6.2 Connect PC to a WiFi device and find the assigned IP address with the command below:


     <!-->
         nano ~/.bashrc

![image](https://user-images.githubusercontent.com/85820553/128559414-f3b76f62-9d0d-44fc-b1bb-76e5deaac302.png)



1.6.3 Press Ctrl+END or Alt+/ to move the cursor to the end of line.
Modify the address of localhost in the ROS_MASTER_URI and ROS_HOSTNAME with the IP address acquired from the above terminal window.

