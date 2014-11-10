ECE382_Lab5_Her
===============

Lab 5, using infared controller to control MSP430


###Objective and Purpose
Use knowledge of interrupts and the Timer_A subsystem to reverse engineer a remote control.

Required Functionality [COMPLETED]:
  
   Required functionality: Turn an led on and off on the MSP430 with a designated button on the remote, and do it again for
   a different led and designated button.
   
   Click on link-->
   ![alt text](https://github.com/vipersfly23/ECE382_Lab5_Her/blob/master/FunctionalityVideo.mp4?raw=true "HEADER CODE")
   
A  Functionality [INCOMPLETE]:
  
    
  
###Implementation  

  Implementation was simply using the interrupts to detect when the IR sensor was sensing a signal and using that to create
  if and else statements for negative and positive edges. From their, the amount of counts per micro-second must be detected
  to use proper delays, and to pre-determine the values for each button. Using the Oscilliscope is dentrimental to analysis 
  of the packet, before coding. Afterwards, the code was straight forward in turning the timer on and off at an appropriate
  time. the following image was given, thus simplified the coding.
  
  ![alt text](https://raw.githubusercontent.com/vipersfly23/ECE382_Lab5_Her/master/schematic.jpg "schematic")
###Code

Variable Definitions:

   *  newPacket: Flag that detected if a complete packet was sent through or not.
   *  packetData[48]: used to ensure the correct data was being sent through. Stored all counts
   *  packetIndex: used to store values into the packetData.
   *  irPacket: stored the code for the button pressed
   
  
Coding is simple, and could be found via file main.c

##Result
  
 Though time didn't permit for A functionality, the required functionality was a success. The buttons worked great, though if
 held too long, multiple packets would be sent. I believe that is specific to this remote. Overall, the lab met the required
 functionality, and objective of using Timer_A subsystem was a success.

###Debugging/Testing

#####Methodology

  
    My methodology was simplicity. I wanted to ensure that I didn't over complicate this lab and the coding involved so I kept to simple if and else statements and ensured I fully understood all the coding and components of the lab. Though I understood everything, there was an error that I did not account for. 
    For some reason, the code was not working properly. I don't understand why, but it wasn't working in class, when I tried to work on it again in my room, it was functioning. I didn't change anything. I'm assuming the system just needed a hard reset. Other than that, the lab went fine, and my understanding of the lab improved drastically from trying to figure out why the program wasn't working.
    
#####Commit 1

 Functioning required functionality.
  
#####Commit 2
  
   Adding Video
   
#####Commit 3
    
  Adding schematic image.
    
****All other commits are either to add comments to the program or to update the README file****

#####Testing:

The program worked great, video provided earlier provides proof.


###Conclusions/Lessons Learned
  In conclusion the program was a success. Lesson learned is to actually restart the system if all attempts been used.
  Sometimes the system just needs a good reset. Other than that, understanding the lab decreased time spent on it.

####Documentation:
  I used the ECE382.com website to access lab information and used the website to obtain the instruction sheet for the assembly
  language. I referenced the code from lecture 26 and built my code from the given nokia.asm and start5.c files. 
  
