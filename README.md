# gaitrehabtools
Therapy rehabilitation is categorized as cardiopulmonary, neurological and musculoskeletal. This research focus on rehabilitation robots for musculoskeletal therapy which assists in strengthening and restoring functionality and improving coordination in the musculoskeletal system. Therapy rehabilitation robots are mainly involved on different actuation systems, degree of intelligence and virtual reality based rehabilitation robots.
The main objective of the research was to develop a complete hardware and software co-design to obtain gait parameters of walking gait to determine the presence of pathologies. The sub divisions of the objectives are as follows:
-	Identification of sensors to obtain gait parameters in terms of kinetic and kinematic parameters
-	Development of a wearable sensory system to acquire gait parameters
-	Development of a gait phase detection algorithm to detect gait phases of walking gait based on kinetic and kinematic parameters
-	Identify pathological gait and the instance of abnormality occurrence based on the gait phases detected
-	Conduct experiments to test and validate the behavior of the developed algorithm for normal and abnormal gait.
-	Test the accuracy of the detected gait phases in comparison to normative data

Hardware Used
Four force sensitive resistors and signal conditioning circuit 
Four force sensitive resistors (FSR) from Interlink Electronics [1] were used to obtain foot pressure patterns during walking gait
A voltage divider circuit was constructed for the conversion of change in resistance to voltage 
LM324 Low Quad Operation Amplifiers were used to amplify the voltage readings obtained from the voltage divider circuit
USB Data Acquisition Device by National Instruments was used to transmit the FSR signals to the host PC. 

Two Inertial Measurement Units (IMU) 
Two Inertia Link IMUs offered by Microstrain [2] to obtain knee joint angle. Inertial Link is a wireless sensor unit with a combination of tri axial accelerometer, tri axial gyroscope, temperature sensors and an on-board processor. The Wireless sensors come with a USB base station which allows efficient data transfer from sensor to host PC

Software Used
LabVIEW
The primary software used was LabVIEW offered by National Instruments to develop a complete gait analysis and gait phase detection system
-	Real time Data Acquisition from all sensors at a sampling rate of 100Hz
-	Signal Processing and Filtering to obtain foot pressure patterns and knee joint angle
-	Gait phase detection algorithm to detect gait phases in real time
-	Development of a second algorithm to determine the instance of abnormality occurrence
-	Development of a graphical user interface 

MatLAB
The gait phase detection algorithm was initially developed using the MatLAB Fuzzy Logic Toolbox and later converted in to LabVIEW

Inertia Link Software
The Inertia Link Software provided by Microstrain was initially utilized to familiarize with the Inertia Link sensor units and the sensor data. 

