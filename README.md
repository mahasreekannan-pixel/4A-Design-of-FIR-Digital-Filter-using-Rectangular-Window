# FIR-FILTER-DESIGN
# EXP 4 A: Design-of-FIR-Digital-Filter-using-Rectangular-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Rectangular-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
<br>clc ; 
<br>close ; 
<br>M=input('Enter the Odd Filter Length ='); 
<br>Wc=input('Enter the Digital Cut off frequency ='); 
<br>alpha= (M -1)/2 // Center Value 
<br>for n = 1:M 
<br>if (n ==alpha+1) 
<br>hd(n) = Wc/ %pi ; 
<br>else 
<br>hd(n) = sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
<br>end 
<br>end 
<br>// Rectangular Window 
<br>for n = 1:M 
<br>W(n) = 1; 
<br>end 
<br>//Windowing filter coefficients 
<br>h = hd.*W; 
<br>disp(h,'Filter Coefficients are') 
<br>[hzm,fr]= frmag (h,256) ; 
<br>subplot(2 ,1 ,1) 
<br>plot(2*fr, hzm) 
<br>xlabel( ' Normalized Digital Frequency w'); 
<br>ylabel( 'Magnitude '); 
<br>title( ' Frequency Response of  FIR LPF using Rectangular Window ') 
<br>hzm_dB = 20* log10 (hzm); 
<br>subplot (2 ,1 ,2); 
<br>plot(2*fr , hzm_dB); 
<br>xlabel( ' Normalized Digital Frequency W' ); 
<br>ylabel( 'Magnitude in dB'); 
<br>title('Frequency Response of FIR LPF using Rectangular Window');

# OUTPUT: 
<img width="630" height="323" alt="image" src="https://github.com/user-attachments/assets/70f21c22-de93-4a06-b891-bdf58b9eac86" />
<img width="458" height="374" alt="image" src="https://github.com/user-attachments/assets/9299b19c-616b-4b53-886d-a790375dd1b3" />

# RESULT: 

Thus design of low pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
<br>clc ; 
<br>close ; 
<br>M=input('Enter the Odd Filter Length ='); 
<br>Wc=input('Enter the Digital Cut off frequency ='); 
<br>alpha= (M -1)/2 // Center Value 
<br>for n = 1:M 
<br>if (n ==alpha+1) 
<br>hd(n)=1-Wc/ %pi ; 
<br>else 
<br>hd(n) =-sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
<br>end 
<br>end 
<br>// Rectangular Window 
<br>for n = 1:M 
<br>W(n) =1; 
<br>end 
<br>//Windowing filter coefficients 
<br>h = hd.*W; 
<br>disp(h,'Filter Coefficients are') 
<br>[hzm,fr]= frmag (h,256) ; 
<br>subplot(2 ,1 ,1) 
<br>plot(2*fr, hzm) 
<br>xlabel( ' Normalized Digital Frequency w'); 
<br>ylabel( 'Magnitude '); 
<br>title( ' Frequency Response of  FIR LPF using Rectangular Window ') 
<br>hzm_dB = 20* log10 (hzm); 
<br>subplot (2 ,1 ,2); 
<br>plot(2*fr , hzm_dB); 
<br>xlabel( ' Normalized Digital Frequency W' ); 
<br>ylabel( 'Magnitude in dB'); 
<br>title('Frequency Response of FIR HPF using Rectangular Window');

# OUTPUT: 
<img width="525" height="376" alt="image" src="https://github.com/user-attachments/assets/f150970f-4bd8-4685-812b-3206fb644adc" />

<img width="459" height="375" alt="image" src="https://github.com/user-attachments/assets/1f8d366c-6221-42a3-88aa-f662f7f557bc" />

# RESULT: 
Thus design of HIGH pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 


# OUTPUT: 


# RESULT: 
Thus design of BAND pass FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 


# OUTPUT: 


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Rectangular-Window waveforms were plotted and output was verified.
