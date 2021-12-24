# ranness

This is practice of nonlinear filter which is an example of optimal trajectory generation.

Second_order.slx is for second order filter for online optimal trajectory generation. And the other one is third order one. Figures show below is the result of the simulation of the third order one. It has to mention that I use different signals in these two simulation, so if you want to compare two filters' difference, you have to keep the signal consistent.

![image](https://user-images.githubusercontent.com/58969475/147307038-aa7449a1-5ffe-48f1-94b7-7707d1ed751f.png)

These plots are jerk, acceleration, velocity and position, respectively. Input signal is a sequence of three step functions. According to the result we can know that the plot of acceleration is continuous now. It is obvious that the third order filter is better.

About some parameters(simulation for third order one):

Ts=0.001;

U=5; % in second order, U means the maximum value of acceleration; in third order, it means the maximum value of jerk.

Vmax=2;

Vmin=-3;

Amin=-2;

Amax=2;

It has to mention that, the module named "if" and "if function"  will keep signal as soon as they are triggered. It will remain and will not recover because the signal stops. So in this simulation, I use logical judgment instead of using these two modules. 

It's normal that there exists fluctuations in the plots. It usually happens when the judgment conditions are close to the critical value. But this result still has some noise.
