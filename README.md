# EXPT-6-Simulation-of-Multirate-DSP-using-Decimation-and-Interpolation

# AIM: 
To perform and verify Multirate-DSP-using-Decimation-and-Interpolation.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc; 
clear; 
close; 

x = [10, 20, 30, 40, 50, 60, 70]; 
n_x = 0:1:(length(x)-1); 

M = 3; 
y_dec = x(1:M:$); 
n_dec = 0:1:(length(y_dec)-1); 

L = 3; 
y_int = zeros(1, L * length(x)); 
y_int(1:L:$) = x; 
n_int = 0:1:(length(y_int)-1); 

figure; 
subplot(3, 1, 1); 
plot2d3(n_x, x); 
h1 = gce(); 
h1.children(1).thickness = 3; 
plot(n_x, x, 'ro'); 
h2 = gce(); 
h2.children(1).thickness = 2; 
h2.children(1).mark_size = 3; 
xtitle('Original Finite Signal', 'n', 'x(n)'); 
xgrid(1); 

subplot(3, 1, 2); 
plot2d3(n_dec, y_dec); 
h3 = gce();
h3.children(1).thickness = 3; 
plot(n_dec, y_dec, 'ro'); 
h4 = gce(); 
h4.children(1).thickness = 2; 
h4.children(1).mark_size = 3; 
xtitle('Decimated Signal (M=3)', 'n', 'y(n)'); 
xgrid(1); 

subplot(3, 1, 3); 
plot2d3(n_int, y_int); 
h5 = gce(); 
h5.children(1).thickness = 3; 
plot(n_int, y_int, 'ro'); 
h6 = gce(); 
h6.children(1).thickness = 2; 
h6.children(1).mark_size = 3; 
xtitle('Interpolated Signal (L=3)', 'n', 'y(n)'); 
xgrid(1);
```

# OUTPUT: 
<img width="1917" height="895" alt="image" src="https://github.com/user-attachments/assets/aee56416-8313-4896-8399-e69bdc0da043" />

# RESULT: 
Thus the Multirate-DSP-using-Decimation-and-Interpolation using python was performed and verified.
