# EXPT 1: Computation-of-DFT-using-direct-method

## AIM
To perform and verify DFT using direct method by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
### DFT DIRECT METHOD
## PROGRAM 
```
clc; 
clear; 
xn=[1 2 3 4 4 3 2 1]; 
n1=0:1:length(xn)-1; 
subplot(3,1,1); 
plot2d3(n1,xn); 
xlabel('Time n'); 
ylabel('Amplitude xn'); 
title('Input Sequence'); 
j=sqrt(-1); 
N=length(xn); 
Xk=zeros(1,N); 
for k=0:N-1 
for n=0:N-1 
Xk(k+1)=Xk(k+1)+xn(n+1)*exp((-j*2*%pi*k*n)/N); 
end 
end 
disp(Xk) 
K1=0:1:length(Xk)-1; 
magnitude=abs(Xk) 
subplot(3,1,2); 
plot2d3(K1,magnitude); 
xlabel('frequency(Hz)'); 
ylabel('magnitude(gain)'); 
title('magnitude spectrum'); 
angle = atan(imag(Xk),real(Xk)) 
subplot(3,1,3); 
plot2d3(K1,angle); 
xlabel('frequency(Hz)'); 
ylabel('Phase'); 
title('Phase spectrum');
```
### CALCULATIONS:
<img width="978" height="1600" alt="image" src="https://github.com/user-attachments/assets/15eac840-5eff-4117-bb80-e9b895f34f17" />

### SAMPLE OUTPUT:

<img width="1600" height="1200" alt="image" src="https://github.com/user-attachments/assets/b58a16cd-d388-4572-8aed-8875a06c12c8" />


## RESULT:
Thus,  DFT using direct method for two given sequences were performed and its result was verified.

