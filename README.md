# adc
Analog-to-Digital Converter

Okay, here goes an attempt to create an analog to digital converter. 

Constraints:
n quantization levels
input signal is restricted 

Methods:
Use n voltage comparators that compute error between a fixed DC voltage and input signal, and whichever comparator's error is least, assign input signal to that quantization level. 

This method requires n comparators. 
Is there a better way? 

How about a simple voltage dividor network, oh which the input signal voltage is available at it's original value, and at increments of this value. The number of increments (divisions) depend on the number of quantization levels. For example, for a 5-level ADC converter, with input signal range of 0-1V, and digital levels of 0V, 0.2V, 0.4V, 0.6V, 0.8V, 1V, there are 6 quantization levels (n+1). 

So the input signal needs to be available at it's original value, 80%,60%,40% and 20% of its original value. The number of input signal voltage divisions depend on the number of quantization level. 
