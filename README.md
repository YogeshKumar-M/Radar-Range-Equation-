# Radar-Range-Equation
#Aim:

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.

# Theory:
The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

# Procedure:
Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice.

Import Necessary Libraries: Import the math library in Python.

Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation.

Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power.

Calculate the Maximum Range: Use the function to calculate the maximum range of the radar.

Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

# Code:
```asm
lambda = 0.05;      
sigma  = 10;         
pi=3.14;
Pt_vals = 0.5:0.5:20;   
Gt_const = 40;         
Pm_const = 1e-13;       
Rmax_Pt = ((Pt_vals .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*pi)^3 .* Pm_const)).^(1/4);
Gt_vals = 5:2:100;      
Pt_const = 2000;           
Pm_const = 1e-13;       
Rmax_Gt = ((Pt_const .* Gt_vals.^2 .* lambda.^2 .* sigma) ./ ((4*pi)^3 .* Pm_const)).^(1/4);
Pm_vals = logspace(-14, -9, 50);  
Pt_const = 3;          
Gt_const = 40;        
Rmax_Pm = ((Pt_const .* Gt_const.^2 .* lambda.^2 .* sigma) ./ ((4*pi)^3 .* Pm_vals)).^(1/4);
subplot(3,1,1);
plot(Pt_vals, Rmax_Pt);
subplot(3,1,2);
plot(Gt_vals, Rmax_Gt);
subplot(3,1,3);
plot(Pm_vals, Rmax_Pm);

```

# Output Waveform



# Calculation:

# Result:

The Range Radar Equation Sucessfully Executed.

