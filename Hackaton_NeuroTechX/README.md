![HackatonPic](https://user-images.githubusercontent.com/71343777/199254748-f1e46d68-49f2-4cab-93ef-1212a85c138a.png)

  
This was Hackaton hosted at 42shcool Paris and other locations around the world (Munich, Belgrade, San-Francisco, New-York...)     
It took place on the last week-end of october.  
    
Teams of 3 to 5 persons  
We were provided with a Bitalino Plugged Kit which we used as a hub were we connected all the measurement devices.   
As measurement devices we had :  
- 1 ECG (électrocardiogramme).
- 1 EEG (électroencéphalogramme).
- 1 EMG (électromyogramme).


![Bitalino_Pic](https://user-images.githubusercontent.com/71343777/199256490-2252406d-760c-48ae-8733-235c2c87f432.jpg)

![Material_Pic](https://user-images.githubusercontent.com/71343777/199256496-e562c353-2f66-4962-8ac9-b939f12533b0.jpg)

Our idea was to use the metrics given by this devices to make a game that will repsond to specific triggers seet for particuliaar Biomarkers.  
(ie : A 2d platformer Game where gameSpeed is regulated by heartrate and may more). We were also planning if we had time to make a VR visualizer for all this Biomarkers with an artistic way of display.

In order to connect Bitalino Device We had to use Anaconda to make a specific environnement with python installed were we could start TimefluxPluggin.  
A pluggin allowing to recover and automatically apply filters to raw data making it easier to understand.   
https://timeflux.io/  
  
As we were not used to anaconda and Yaml (language use to configurate Timeflux) it took us a bit of time to be abble to display something first of all.  
Display on terminal : 
    
![DispBit](https://user-images.githubusercontent.com/71343777/199263888-ee8965ab-c1a1-4f07-a0f3-363ac0a63881.png)

Then We manage to use Display UI node to show data on Browser UI (The data displayed is a sine curve as we forgot to take pictures of this we had the Bitalino Device)
![UiBit](https://user-images.githubusercontent.com/71343777/199263893-b4563365-d33d-43f2-81ea-2121a7ee5d44.png)

We then understood that we will not be able to use this data as a lot of processing was necessary to recover "real" data from the devices.  
So we choosed to use Timeflux Demos and send data from those components to Unity through socket with LSL. 
Link to Demo repositoriies : https://github.com/timeflux/demos
We also had to figure out how LSL nodes and library works (from timeflux and unity).

First Results on unity : Cylinder X-axis Scale Linked to Hearthbeat Rate using Coherence Demo (disrigard the sound of the video we were excited).
https://user-images.githubusercontent.com/71343777/199258373-c6424557-98f3-4079-a0f4-9798ce390f09.mp4

As we were running short on time we choosed to abandon the gaame project and focused on a way to link Biomarkers with artistic displays (without VR).   
We choosed to use a teechnique desribed in this video using screen shaders : https://www.youtube.com/watch?v=X-iSQQgOd1A&ab_channel=SebastianLague
  
Best Result we've had : HearthBeat connected to Speed, Detection and turn radius of the cells (sorry for the bad quality) : 

  https://user-images.githubusercontent.com/71343777/199266723-017a8524-c7f5-4cc9-aff9-9e9f30323961.mp4


Possible Improvements :
- Using The Roshambo demo from timeflux in order to use EMG to understand if user is doing Rock Paper Scissors  and then use it as a selector between diffrent cell species (the different colors of cells you see on screen). Something like rock=sp1 scissors=sp2 paperr=sp3 nothing=all species
-  Using The Neuro_feedback demo from timeflux in order to use EEG to get brainWaves and use them to modify color and behaviour of species.

This was really fun and interesting and we may go back  to this project to implement some improvement.
Thanks for reading this, if you are interested in source code contact me by mail : t.scandolera@gmail.com 
