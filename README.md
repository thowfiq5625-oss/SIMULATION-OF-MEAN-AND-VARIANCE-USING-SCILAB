# SIMULATION-OF-MEAN-AND-VARIANCE-USING-SCILAB
## AIM
To write a program for mean, variance and cross correlation in SCILAB and verify the output.

## EQUIPMENTS NEEDED

•	Computer with i3 Processor
•	SCI LAB


## ALGORITHM
1.	Define	the	Function:	Specify the	function	you	want	to	simulate.	For	example, f(x)=sin⁡(x)f(x) = \sin(x)f(x)=sin(x) or any other function.
2.	Generate Sample Points: Decide on the range and the number of sample points. Generate these sample points within the desired range.
3.	Evaluate the Function: Compute the function values at each of these sample points.
4.	Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean and variance of the computed function values.
5.	Display Results: Output the computed mean variance and Cross Correlation
   
## PROCEDURE
•	Refer Algorithms and write code for the experiment.

•	Open SCILAB in System

•	Type your code in New Editor

•	Save the file

•	Execute the code

•	If any Error, correct it in code and execute again

•	Verify the generated results


## PROGRAM
clc;

 clear;
 
  function fx = pdfx(x)
  
      z = 3*(1-x)^2;
      
      fx = x*z;
  
  endfunction
  
  a = 0;
  
  b = 1;
  
  EX = intg(a, b, pdfx);
  
  function fy = pdfy(x)
  
      z = 6*(1-x)^2;
      
      fy = x*z;
  
  endfunction
  
  EY = intg(a, b, pdfy);
  
  disp("1)Mean of X =",EX);
  
  disp("2)Mean of Y =",EY);
  
  function p = f1(u)
      
      q = 3*(1-u)^2;
      
      p = u^2 * q;
  
  endfunction
  
  a = 0;
 
  b = 1;
  
  EX2 = intg(a, b, f1);
  
  function r = f2(v)
  
      s = 6*(1-v)^2;
     
      r = v^2 * s;
  
  endfunction
  
  EY2 = intg(a, b, f2);
  
  vX2 = EX2 - (EX)^2;
 
  vY2 = EY2 - (EY)^2;
  
  disp("3) Variance of X =",vX2);
  
  disp("4)Variance of Y =",vY2);
  
  
  x= input("type in the reference sequence=");
  
  y= input("type in the second sequence=");
  
  S1=max(size(y))-1;
  
  S2=max(size(x))-1;
  
  r=corr(x,y,S1);
  
  plot2d3('gnn',r);
## CALCULATION
![WhatsApp Image 2025-11-19 at 17 51 37_78f58b78](https://github.com/user-attachments/assets/7524e6db-b43e-4568-b090-de037445a6ad)
## OUTPUT
![WhatsApp Image 2025-11-19 at 17 52 15_b52d3979](https://github.com/user-attachments/assets/67abd7f3-00bd-4246-bc84-faa509d8028e)

![WhatsApp Image 2025-11-19 at 17 54 57_9f20fa09](https://github.com/user-attachments/assets/8a3c266b-22f7-4eb2-88a5-f71918834e1c)

## RESULT

Thus, the Mean,Variance and cross correlation are executed in Scilab and output is verified.
