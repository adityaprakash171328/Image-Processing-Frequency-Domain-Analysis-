# Image-Processing-Frequency-Domain-Analysis-
Magnitude Spectra Analysis: 
The Python code successfully computed the 2D 
Fourier transform of the cat image and displayed 
the magnitude spectra in both normal and dB 
forms. The magnitude spectrum represents the 
amplitude of frequency components, while the dB 
form (20*log10) provides better visualization of 
the dynamic range. 

Spectrum Centering: 
By default, the zero frequency component (DC 
component) is located at the corners of the 
spectrum. The fftshift function centers the low 
frequencies by moving the zero frequency 
component to the center of the 2D transform. This 
centering is achieved by rearranging the 
quadrants of the frequency domain 
representation. 

Rotation Analysis: 
When the input image is rotated anti-clockwise by 
90 degrees, the magnitude spectrum also rotates 
by the same angle. This demonstrates the rotation 
property of the Fourier transform: rotating the 
spatial domain image by angle theta rotates the 
frequency domain by the same angle theta. 
Key Observation: The magnitude spectrum 
preserves the rotational relationship between 
spatial and frequency domains, which is a 
fundamental property of the 2D Fourier transform. 
The frequency content structure remains intact but 
oriented according to the spatial rotation. 

Frequency Mixer System: 
The frequency mixer system creatively fuses two 
images by combining different frequency 
components from each source: 
System Design: 
• Low frequencies from Image 1 (cat): Provides 
overall structure and illumination. 
• High frequencies from Image 2 (dog): 
Provides fine details and texture 

Implementation: 
The system uses a circular low-pass filter mask 
with radius 30 pixels. 

Transfer Function Analysis: 
The frequency mixer employs two complementary 
Transfer functions: 
Transfer Function Properties: 
The low-pass filter has a value of 1 inside the 
circular region and 0 outside 
The high-pass filter has a value of 0 inside the 
circular region and 1 outside 
Together, they form a complete frequency 
domain partition: H_low + H_high = 1 

Cutoff frequency: Determined by the circular 
mask radius 

Filter shape: Circular (isotropic) for uniform 
frequency response in all directions 

Fusion method: Linear addition of filtered 
frequency components 

The resulting fused image combines the structural 
foundation from one image with the detailed 
texture from another, creating a perceptually 
interesting hybrid that leverages different 
frequency bands for different types of visual 
information.

Observations: 

1. The spectrum is centered using fftshift - 
low frequencies are at the center. 

2. Rotating the image by 90° also rotates its 
spectrum by 90°. 

3. The frequency mixer combines structural 
info (low freq) from cat with details (high 
freq) from dog. 

4. The fused image shows the overall 
shape/illumination of the cat with fine 
details from the dog.
