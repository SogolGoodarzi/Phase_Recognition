# Phase_Recognition
<p align="justify"> There is a common belief that the human ear is not able to hear the phase. That is, it cannot distinguish two signals with different phases. We want to test this hypothesis. For this purpose, we design an LTI system that does not change the size of the input but changes its phase. In general, such systems are called "all-pass systems". </p>

Consider the following all-pass system:

![image](https://github.com/SogolGoodarzi/Phase_Recognition/assets/125180530/8c11071a-8ca6-403e-b325-96397470a011)

1. We plot the amplitude and phase of this system for N=1 with the use of "freqz" function. Then with the use of "zplane" funtion we show the zeros and poles of this system. 

![image](https://github.com/SogolGoodarzi/Phase_Recognition/assets/125180530/55b6576d-8e95-40be-96dd-4b511b1cc430)

![image](https://github.com/SogolGoodarzi/Phase_Recognition/assets/125180530/c96ae9a5-d65d-4bb7-b648-cc817b958ac0)

<p align="justify"> 2. Now, with the help of "filter" function, find the output of this system for the "speech.wav" audio signal input and save it in an audio file called "output1.wav". So, if we listen to the output file or the filtered signal, we will not feel much difference from the original sound. This is because the system does not resize. As it is clear from the diagram, the amplitude of the system has a constant value of 1 at all times, so because of this constant, our ears hear the sound correctly. According to the phase diagram, it is clear that the system changes the phase a little, but not so much that our ears are sensitive to it and cannot hear or feel a change in the sound. </p>

It should be noted that in this case the poles of the system are inside the unit circle, so the system is stable.

<p align="justify"> 3. Now we want to change the input phase more in a way that the changes can be noticed. So, we repeat doing the previous parts for N=15. The results are shown in the following figures. </p>

![image](https://github.com/SogolGoodarzi/Phase_Recognition/assets/125180530/cb506203-3db8-4ad1-b2be-41d334b84500)

![image](https://github.com/SogolGoodarzi/Phase_Recognition/assets/125180530/fc1db226-88b0-4d78-8c64-3ae6bc622c1f)

<p align="justify"> As it is clear from the zero and pole graph drawn, we can see that according to the rule of the system when N=15, we expect zero and the poles obtained for N=1 to be repeated 15 times in this case, or in other words, 15 poles and repeated zeros. But what can be seen from the graph is that the poles and zeros are not on top of each other and there is some dispersion between them. So, as we expected, we can say that the graph of zero and poles of this section is not drawn correctly. </p>

<p align="justify"> 4. For the audio file used in part 2, we do the same process for the new system (with N=15) and save the output file which named "output2.wav". If we listen to the output, we see no difference between the original signal and the filtered signal. Based on the system size diagram, as it is clear from the figure, the disturbance created at the end frequencies of the diagram have a small range and are of the order of $10^{-5}$, which is a very small amount. So it can be said that these disturbances will not make much difference compared to the size of the system which was drawn in the first part and was all 1. Also, for the phase, if you pay close attention, the phase diagram drawn in this state is not very different from the state where N=1 (it means a difference that can be understood by the human ear). For this reason, the signals heard in the two parts do not differ much. Also, if you pay attention to the graph of zero and poles, you can see that the poles are still inside the unit circle, so the system is stable and we hear the sound correctly. Up to this part, where we hear the sound as the original sound, then our ears have been able to hear the phase. </p>

5. Now it's time to repeat the parts for another value of N which is N=50. The results are shown below.

![image](https://github.com/SogolGoodarzi/Phase_Recognition/assets/125180530/b760b129-f657-4bc1-8c00-27d0fddec6e0)

![image](https://github.com/SogolGoodarzi/Phase_Recognition/assets/125180530/9054bff7-7db8-425b-a525-1dc40142bac1)

<p align="justify"> As it is clear, in this case, similarly to the third part, the pole and zero diagram is not drawn correctly. The reason for this here is similar to the argument that was said in the third part. </p>

<p align="justify"> If we listen to the filtered output signal, in this case we will hear a sound like a horn and we will no longer be able to hear the same sound as in the previous parts. So, in this case, our ears cannot hear the phase. In this case, if we pay attention to the size diagram of the system, we can see that in the frequencies where the size diagram is disturbed, the range of values ​​is much larger than the previous state, which was in the order of $10^{-5}$, and the ranges are almost in the order of 10 and 20. So here, because there is a big difference in the size of the system, our ears also find a significant difference in the sound heard. Also, for the shape of the drawn phase diagram, it can be said that in this case, for N=50, because the phase diagram is slightly different from the phase diagram drawn in the previous two parts, for this reason, it can be said that the audible frequency range in this case for N =50 is slightly different from the previous two modes, but the main reason that we did not hear the sound properly is related to the size of the system as explained. Also, if we pay attention to the drawn zero and pole diagram, the poles are not placed inside the unit circle and that is why the system is unstable, so this is another reason why we cannot recognize the sound correctly.</p>
