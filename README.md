###  DATE: 22/04/2024

###  NAME: PONRAJ M
###  ROLL NO : 212221080055
###  DEPARTMENT: MECHANICAL
# Experiment-no-6-DC-Motor-Speed-Control-Using-Arduino
### AIM : To control the speed and the direction of a DC motor using L293D driver ic( H- bridge)

### Components Required:
•	Arduino UNO board
•	L293D driver
•	12V DC motor
•	10K ohm potentiometer
•	Pushbutton
•	12V source
•	Breadboard
•	Jumper wires
### THEORY 
The L293D quadruple half-H drivers chip allows us to drive 2 motors in both directions, with two PWM outputs from the Arduino we can easily control the speed as well as the direction of rotation of one DC motor. (PWM: Pulse Width Modulation).
Arduino DC motor control circuit:
Project circuit schematic diagram is the one below.
![image](https://github.com/vasanthkumarch/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/161028709/763b4370-3496-45b9-a029-41307f1f8f4a)
![image](https://github.com/vasanthkumarch/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/161028709/29d7329b-b978-43ac-a03f-3e727eaaa169)
![image](https://github.com/vasanthkumarch/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/161028709/18ba9d29-66fe-45ca-b8bf-8fb871a08e3e)



FIGURE-01 H BRIDGE CIRUCIT INTERFACE 
 
The speed of the DC motor (both directions) is controlled with the 10k potentiometer which is connected to analog channel 0 (A0) and the direction of rotation is controlled with the push button which is connected to pin 8 of the Arduino UNO board. If the button is pressed the motor will change its direction directly.
The L293D driver has 2 VCCs: VCC1 is +5V and VCC2 is +12V (same as motor nominal voltage). Pins IN1 and IN2 are the control pins where:
![image](https://user-images.githubusercontent.com/36288975/167763120-1421c2c5-8381-49eb-b376-03f6e1113b7a.png)
TABLE-01 EXITATION TABLE FOR H BRIDGE 

As shown in the circuit diagram we need only 3 Arduino terminal pins, pin 8 is for the push button which toggles the motor direction of rotation. Pins 9 and 10 are PWM signal outputs, at any time there is only 1 active PWM, this allows us to control the direction as well as the speed by varying the duty cycle of the PWM signal. The active PWM pin decides the motor direction of rotation (one at a time, the other output is logic 0).

### PROGRAM 
~~~~
int in1=5;

int in2=6;

int en=3;

void setup()

{

pinMode(in1,OUTPUT);

pinMode(in2,OUTPUT);

pinMode(en,OUTPUT);

}

void loop()

{

analogWrite(en,50);

digitalWrite(in2, LOW);

digitalWrite(in2, HIGH);

delay(100);

}
~~~
### OUTPUT

### GRAPH AND TABULATION 

![image](https://github.com/vasanthkumarch/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/161028709/e644bc9d-24ac-4c0e-9330-239715626183)
![image](https://github.com/vasanthkumarch/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/161028709/0bda51aa-545a-46e9-a9a0-3e2dbd0963dd)


### RESULTS AND DISCUSSION 
The speed and the direction of a DC motor using L293D driver ic( H- bridge) is controlled and studied
