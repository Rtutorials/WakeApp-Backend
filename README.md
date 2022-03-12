# WakeApp (Backend)

For the ITC transportation hackathon we built WakeApp: It detects if a driver has fallen asleep at the wheel and wakes them up. We won first prize! 🥇

Take a look at our presentation <a href=https://youtu.be/fTslVKN8JVU>Video!</a> 


<img width="565" alt="Screen Shot 2022-03-12 at 8 30 34 PM" src="https://user-images.githubusercontent.com/19825656/158030294-e58abad5-df45-4a3c-8e6a-01ff1061ddcb.png">

<img width="561" alt="Screen Shot 2022-03-12 at 8 31 03 PM" src="https://user-images.githubusercontent.com/19825656/158030315-62fd8ebf-9583-4e1d-8099-76162702a7b4.png">


The idea is that your phone camera takes repeated fast pictures and detects eye locations and if the eyes are closed using a CNN. If eyes are confidently determined to be closed for a few seconds a wake up sound is played- If you have any questions or ideas on how to use or improve this technology, do shoot a message.

![image (9)](https://user-images.githubusercontent.com/19825656/158031418-aeb5bb2b-db15-4415-a497-78d15b93b309.png)

The images were trained on 57,000 eye images, half open half closed. The data can be found at http://mrl.cs.vsb.cz/eyedataset. The first task is eye detection, which was achieved using a haar cascade (90% accuracy). The second task was cropping the image to just the frame of the eyes and adjusting for bright/dark images. The third task was labeling eyes as open/closed (98% accuracy). Putting it all together is a NodeJS frontend which accesses a camera pointed at the user and takes a photo multiple times a second and sends it to a flask server running this code. If eyes are consistently not detected as open for several seconds in a row, a loud sound is played to the user.


<img width="556" alt="Screen Shot 2022-03-12 at 8 28 54 PM" src="https://user-images.githubusercontent.com/19825656/158030225-d89acb4d-dd06-4069-aa1b-590d41e16876.png">


Thank you ITC and teammates Benjamin Dahan, David Frisher, Bailey Hassall, Golda Hutchison, Aviad S. and Oz Ziv

#hackathon #computervision  #coding #programming #transport #machinelearning
https://lnkd.in/dZdQt7ah




