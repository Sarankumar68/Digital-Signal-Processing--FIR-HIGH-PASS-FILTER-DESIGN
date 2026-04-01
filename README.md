# Digital-Signal-Processing--FIR-HIGH-PASS-FILTER-DESIGN
## AIM:
To generate design of High pass FIR digital filter using Window.
## Software Required:
MAT LAB R2012.
## Algorithm:
Step 1: Open MATLAB and Write the program.

Step 2: Read the values of cut off frequency wc.

Step 2: Read the values of Order of the filter N.

Step 3: Find out the desired impulse response of the hIGH Pass filter Coefficient.

Step 4: Find out the windowing sequence.

Step 5: Plot the magnitude spectrum with x-label and y-label with suitable title.

Step 6: Terminate the program.

## PROGRAM: 
```
clc; % clear screen
clear all; % clear screen
close all; % close all figure windows
wc1=input('enter the value of wc1');
wc2=input('enter the value of wc2');
N=input('enter the value of filter');
alpha=(N-1)/2;
eps=0.001;
%Band Stop Filter Coefficient 
n=0:1:N-1;
hd=(sin(pi*(n-alpha+eps))-sin((n-alpha+eps)*wc1)+sin((n-alpha+eps)*wc2))./(pi*(n-alpha+eps)) 
%Hamming Window Sequence
n=0:1:N-1;
wh=0.54-0.46*cos((2*pi*n)/(N-1))
hn=hd.*wh
% Plot the Low Pass Filter with Hamming Window Technique
w=0:0.01:pi;
h=freqz(hn,1,w);
plot(w/pi,abs(h),'blue');
title('Band Stop FIR Filter using Hamming Window');
```

## OUTPUT:

![WhatsApp Image 2026-04-01 at 3 42 53 PM](https://github.com/user-attachments/assets/46759f84-0dcc-4f74-9102-57b8c42d60b8)

## RESULT:

![WhatsApp Image 2026-04-01 at 3 20 03 PM](https://github.com/user-attachments/assets/f4ac3095-985f-4d84-8c42-68ede76f6790)

