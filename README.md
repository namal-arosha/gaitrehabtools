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

Instruction Manual for the Real-time Software Application

Note: The real-time software application will function without errors only if the NIDAQmx and the SQL Server 2005 is installed with the database. The Inertia Link Units as well as the instrument shoe insole should be attached to the host PC, in order to acquire gait parameters.
Tab 1: Create/view personal information

This tab is dedicated to deal with personal information of patients as well as creating new trial records of patients, before moving on to the acquisition of data, or data analysis. 
New Record -	Add personal information for a patient who is new to the overall system. The ID field is automatically updated by the system. 
Existing Records - 	If the patient already exists in the database, this tab allows user to view personal records of the patient. Historical records of the trials can also be viewed by activating the “View Historical Record” button, which will take you to tab 5 (discussed further in tab 5).
Trial Records -	Prior to starting the rehabilitation procedure, it is required to create a trial record for the patient. This can be achieved by executing the “Create New Trial” button. 
Tab 2:  Sensor setup and Testing

Tab 2 allows user to setup the hardware and verify the workability of the wearable device before proceeding to data acquisition.
Step 1: 	Select the Channels of the NIDAQmx which the four FSRs are connected. Select the com ports and the corresponding node addresses of the Inertia Link. 
Step 2: 	The left plot graphically represents the four FSR signals separately, which allows to check the workability of each FSR. The gauges on the right represent the Euler angles about X, Y and Z axes respectively, for each Inertia Link. This enables zero referencing for each Inertia Link. 

Tab 3: Data Acquisition

Once the overall hardware system is verified, tab 3 allows user to acquire data from the wearable system. 
Step 1: 	The single and multiple selection button allows user to select the acquisition of data from one sensor type or both, respectively. 
Step 2:	If “single sensor type” selection is ON the system allows acquisition of only one sensor type at a time. The selected sensor data will be graphically represented to the user. However real time gait phase detection will not occur due to insufficient data to run the algorithm. A message will be displayed to the user, upon the selection of “single sensor type” to notify the user that the gait phase plots will not be represented for this selection.  
Step 3: 	If “multiple sensor typle” selection is ON, the system allows the acquisition of both sensor types, and the sensor data will be graphically represented for each FSR signal and the Knee Angle. The gait phase plots will also be plotted in the right hand plot in real time. 
All sensor data will be saved in to a file for later reference. 
Tab 4: Post Analysis 

The post analysis tab allows user to compare and contrast trial records of two patients are two different trial records of the same patient. 
Step 1: 	The trial records in the database are represented to the user in the two drop down menus. The user will be allowed to choose two trial records of two patients or the same patient. Upon activating the “Plot” button, the sum of the foot pressure signals and the knee angle will be represented to the user in graphical format. 
Step 2: 	Four cursors are available which allows the user to select one gait cycle of each trial record. “Red” cursors should be used to select a gait cycle of “Subject 1” and the “Green” cursors should be used to select a gait cycle of “Subject 2.”
Step 3: 	Upon activating the “Sync” button, the system will automatically synchronize the selected gait cycles as a percentage. The foot pressure patterns, knee angle and the gait phase plots are displayed to the user for better comparison. 
Tab 5: Report summary of trial records of a patient

Tab 5 allows the user to view historical records of a selected patient. The personal information along with the trial records saved in the database is displayed to the user. 
Step 1: 	Select the patient name from the drop down menu to obtain personal information and trial records. The details of the trial records will be displayed in table format. 
Step 2: 	The foot pressure patterns and the knee angle for each trial could be viewed by clicking on the “Link File” column of the selected record. 
Step 3: 	Each trial record could be deleted by clicking on the last column of a selected row. 
Step 4: 	The complete patient record could also be deleted by activating the “Delete Patient Records” button. 


