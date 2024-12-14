# GunShot-Detection

This Project of mine is implemented to dectect the Direction of the GunShots in any envionment. This model optimally detect the Direction of the GunShot Sourse through the series of algorithms.
The Accuracy of the model is mean found by simple 5 Steps of Process.

Step 1: Microphone Array Setup

The Microphone captures the Sound Sourse(Gunshots) from any environments like battlefields,wild life,public or private areas. The Microphone setup Consists of 6 Microphones that covers the complete 360 Degree.Those 6 microphones will Capture the sound and through few algrithms the direction is detected. 

Step 2: Analog to Digital Converstion 

The Analog to Digital converstion is performed by converting analog signals into digital signals.This process will be progressing after the "Normalization" of the signals is mode.The normalizing the signals would help the signals to get processed easily that means the signal will be normalized to the Range [-1 to 1].ADC converstion now converts the continous signals to Discrete Digital signals.

Step 3: Digital Signal Processing 

The Signals will have all wanted(Gunshot Hz) and unwanted frequency(external sound/noise Hz),In Digital Signal Processing the filtering of the needed frequency is done.From my observation the approx Frequency of a GunShot is ranged from 2500 Hz to 3500 Hz,So the BandPass Filtering is the Solution for Filtering the gunshots.The BandPass Filtering will be picking the Signals thats in the range of 2500 Hz to 3500Hz.The filtered Signal will be taken separatly for detecting the direction.

Step 4: Field Programmable Gate Array Algorithms(FPGA):

  i)Signal Classification:
  
  The filtered Signal is classified as different methods like Frequency,WaveForm,Hz,Aplitude.The classification in my model is done and it shows the gunshot is detected or not by the classified signals.
  
  ii)Signal Localization:
  
  The localization is the process where the direction of the gunshot is been found.This localization will perform a TDoA algorithm(Time Difference of Arrival).The concept is simple, each microphone will capture the same signal in different timeline so,the time difference is calculated between each microphones and the greater the aplitude then the direction is futher found.Co-realtion between microphones is done to find the high value of aplitude for direction detection.

Step 5: Graphcial Display

Now the detected direction wwill bee displayed in the 360 degree graph for easy accessabiltiy.

DataSet:

The datasets are taken from Kaggle.https://www.kaggle.com/datasets.

Feasibility:

1. Technical Feasibility:

FPGA technology and omnidirectional microphones
Sound classification and localization using TDoA

2. Market Feasibility:

Strong demand in military, law enforcement, and private security
Real-time threat awareness as a key selling point

3. Financial Feasibility:

Significant upfront investment for FPGA development and testing
High potential for long-term revenue through military/law enforcement contracts
Recurring income via customization, support, and maintenance agreements

Target Audience:

1.Military Forces
2.Prevention of Hunting WildLife
3.Private Security
4.Border surveillance
5.Public Welfare

Benefits of this Solution:

1.Real-Time Detection(Immediate)
2.High Accuracy(Over 89.7% Accuracy)
3.Frequency Filtering(Only Filtering GunShots Source)
4.Faster Detection due to less Complexity(Effective Algorithms)

MICROPHONE SIGNALS CAPTURED INITIALLY:
![image](https://github.com/user-attachments/assets/18df5690-d50e-4f83-a70d-61e583d8a746)

BANDPASS FILTERING:
![image](https://github.com/user-attachments/assets/b960d907-fbba-43ce-9aa3-59bf3cd9ff83)


DIRECTION DETECIION THROUGH GRAPH:



![image](https://github.com/user-attachments/assets/ec6dcc6c-62cc-42ec-9c64-025aa1daf8db)
