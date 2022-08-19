# Comperator-5V-PWM-to-12V-PWM

!!! It's under construction !!!

The target is to convert a 5V PWM Signal to 12V PWM signal


#Reference Voltage Calculation

The reference voltage should be the half of 5V.
The supplied Voltage is 12V.
The used resistors have 0.6W
We use 2 resistors for the voltage devider.
We want ~ 2.5V as reference voltage. Thant means 12V-2.5V=9.5V at R1

![the circuit](https://github.com/InTheCar/Comperator-5V-PWM-to-12V-PWM/blob/main/pictures/Reference%20Voltage.png)

What's the maximum current for 0.6W resistors?

The most Power will be at R1 because the current at R1 and R2 is the same but the Voltage at R1 ist higher.
P=U*I
I=P/U
I=0.6W / 9,5V
I=63mA
This is the maximum current!! If it's more R1 will be blowed up.

We define a current of 10mA. Both resistors are save with it.

Now we calculte R1 with 9,5V and 10mA:





