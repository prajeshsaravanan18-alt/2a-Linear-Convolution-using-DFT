EXPT 2a: LINEAR CONVOLUTION-USING-DFT
AIM
To perform and verify linear convolution operation of two given sequences using SCILAB.

APPARATUS REQUIRED
PC installed with SCILAB

PROGRAM:
LINEAR CONVOLUTION

clc; 
clear; 
x = [1 2 3 4]; 
h = [2 4 8 6]; 
m = length(x); 
n = length(h); 
a=0:1:m-1; 
b=0:1:n-1; 
subplot(3,1,1); 
plot2d3(a,x); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Graphical Representation of Input Signal X'); 
subplot(3,1,2); 
plot2d3(b,h); 
xlabel('Time'); 
ylabel('Amplitude'); 
title('Graphical Representation of Impulse Signal h'); 
for i = 1: n+m-1 
    conv_sum = 0; 
    for j = 1:i 
        if (((i-j+1) <= n)&(j <=m)) 
            conv_sum = conv_sum + x(j)*h(i-j+1); 
        end; 
        y(i) = conv_sum; 
    end; 
end; 
disp(y,'Convolution Sum using Direct Formula Method = ') 
subplot(3,1,3); 
plot2d3(y) 
title('Graphical Representation of output Signal y');





### CALCULATIONS:

<img width="1004" height="1600" alt="image" src="https://github.com/user-attachments/assets/03cddd36-c9bc-47b8-9353-9eae6079ecff" />
<img width="960" height="1600" alt="image" src="https://github.com/user-attachments/assets/54213562-acad-4ad9-b2d3-95fc3a1a102f" />
<img width="1600" height="773" alt="image" src="https://github.com/user-attachments/assets/c268e742-95f8-4718-bfd6-1bf763d6d8ef" />



### SAMPLE OUTPUT:

<img width="899" height="1599" alt="image" src="https://github.com/user-attachments/assets/16e320fa-5d73-47af-aeb7-1a2a43b95089" />




RESULT:
Thus, the linear convolution of the two given sequences were performed and its result was verified.
