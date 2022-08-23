# Comperator-5V-PWM-to-12V-PWM

!!! It's under construction !!!

The target is to convert a 5V PWM Signal to 12V PWM signal.

The main circuit is from the following web page:

http://www.ne555.at/2014/index.php/schaltungstechnik/390-komparator-mit-lm393.html


## Reference Voltage Calculation

The reference voltage should be the half of 5V.
The supplied Voltage is Usupply=12V.
The used resistors have 0.6W
We use 2 resistors for the voltage divider.
We want ~ 2.5V as reference voltage. Thant means 12V-2.5V=9.5V at R1

![the circuit](https://github.com/InTheCar/Comperator-5V-PWM-to-12V-PWM/blob/main/pictures/Reference%20Voltage.png)

What's the maximum current for 0.6W resistors?

The most Power will be at R1 because the current at R1 and R2 is the same but the Voltage at R1 is higher.
Usupply=U1+U2
12V=9.5V+2.5V
U1=9.5V
U2=2.5V

P=U*I
I=P/U1
I=0.6W / 9,5V
I=63mA
This is the maximum current!! If it's more R1 will be blowed up.

We define a current of 10mA. Both resistors are save with it.

Now we calculte R1 with U1=9.5V and I=0.25mA:

R1=U1/I
R1=9.5V/0.25mA
R1=38k
->
R1=47k

Now we calculate R1 with U2=2.5V and I=0.25mA:

R2=U1/I
R2=2.5V/0.25mA
R2=10k
->
R2=10k

Due to the fact that the calculated resistors are not existing and we choosed the next existing one, we have to do the calculation with the choosen restistors again.
R1=47k
R2=10
Usupply=12V

(R1+R2)=Usupply/I
I=Usupply/(R1+R2)
I=12V/57k
I=0,21mA

And now the calculatuin of Uref:
U2=R2*I
U2=10k*0.21mA
U2=2.1V


## Summarry of the results for the reference Voltage

R1=47k
R2=10k
Uref=2.1V

## The operation amplifier
I choosed the LM393 operation amplifier:

![LM393](https://github.com/InTheCar/Comperator-5V-PWM-to-12V-PWM/blob/main/pictures/LM393.png)

## The circuit
![the circuit](https://github.com/InTheCar/Comperator-5V-PWM-to-12V-PWM/blob/main/pictures/the%20circuit.png)

R1=47k
R2=10k
R3=10k
R4=1M
R5=4K7

## The circuit with real LM393

![the circuit with real LM393](https://github.com/InTheCar/Comperator-5V-PWM-to-12V-PWM/blob/main/pictures/the%20circuit%20with%20real%20LM393.png)

R1=47k
R2=10k
R3=10k
R4=1M
R5=4K7

## The Prototype

A drillen board is used for the prototype.
Here a picture of the used circuit board:
![the Prototype](https://github.com/InTheCar/Comperator-5V-PWM-to-12V-PWM/blob/main/pictures/Prototype%20-%20labels.png)


![the Prototype](https://github.com/InTheCar/Comperator-5V-PWM-to-12V-PWM/blob/main/pictures/Prototype%20-%20labels.png)




