# ServoController-6DOF
ATMEGA2560 Servo controller for use with FlyPT mover and AASD-15A drives

600mm travel actuator with SF1610 ball screw
Scale = 0.9155

"<255><255><a1><a2><a3><0><0>"

Pn2 = 2
Pn8 = 300
Pn9 = -300
Pn51 = 3000 (motor top speed/rpm, could be run slower if wanted)
Pn98 = 10
Pn109 = 1
Pn110 = 30
Pn113 = 20
Pn114 = 10
Pn115 = 100
Extra parameters needed in the AASD-15A drivers used for limits detection:
Pn24 = 100 (reach predetermined torque > 100%)
Pn52 = 1
Pn60 = 2 (not used for now)
Pn61 = 6

AASD-15A CN2 DB25 control signal connector explained:
 p3 - pwm signal
 p4 - direction
 p5 - GND
 p6 - enable (motor ON)
 p9 - 5Vcc
p10 - GND
p11 - ready (motor present and ready - not used for now)
p14 - GND
p23 - torque reached

AASD-15A
CN2 DB25 pin / Arduino pin
Motor 1
 3              12
 4              A0
 6              A4
 23             18 (via 2.2kohm resistor and 0.1uF capacitor to GND)
 9              5Vcc
 5,10,14        GND

Motor 2
 3              2
 4              A1
 6              A5
 23             19 (via 2.2kohm resistor and 0.1uF capacitor to GND)
 9              5Vcc
 5,10,14        GND

Motor 3
 3              7
 4              A2
 6              A6
 23             20 (via 2.2kohm resistor and 0.1uF capacitor to GND)
 9              5Vcc
 5,10,14        GND

Motor 4
 3              45
 4              A3
 6              A7
 23             21 (via 2.2kohm resistor and 0.1uF capacitor to GND)
 9              5Vcc
 5,10,14        GND
  
