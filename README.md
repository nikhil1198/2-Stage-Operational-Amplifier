# 2-Stage-Operational-Amplifier

# Objectives: 

* Complete designs of 2 Stage OP Amps with specifications :
* Open loop gain = 10^6 = 120dB
* Bandwidth = 50 MHz
* Power Voltage Supply (Vdd) = 3.3 V
* Max. Output Swing = Vdd/4 = 0.825 V
* Slew Rate (V/μs) = 1
* Power = 8 mW

# Design Specifications:

* Current Mirrors used for gate biasing of current source loads.
* Golden Current Value ( reference current)
* Differential Pair with Active Load
* PMOS with NMOS load
* Load Capacitance and an additional miller capacitance (Cc) for stability and dominant pole shift.

# Design Description:

* To achieve high gain systems we require two stage op amps as their amplifications get compounded.
* The first stage is a differential pair with active load, followed by the second NMOS load.
* The introduction of two stages causes two capacitances,  at load of both stages making it a two pole system.
* Two avoid instability and reduce oscillations due to poor phase margins  an additional miller capacitance is used to transform the system into effectively an one pole system (by dominant pole shift)
* A reference current is mirrored across the circuit so as to bias currents source loads.

# The Circuit:

![alt text](https://github.com/nikhil1198/2-Stage-Operational-Amplifier/blob/master/circuit.JPG)

# Design Calculations:

* Assumptions and Values used:
  * Single ended output is taken
  * M1 and M2 are identical
  * M3 and M4 are identical
  * Higher current flows in outer circuit to provide high swing, than in the inner circuit
  * µpCox = 50 µAV-2 	   and          µnCox = 100 µAV-2
  * λp = 0.052 V-1                       and          λn = 0.011 V-1
  * Vthp = -0.4 V	                      and          Vthn = 0.4 V
  * Av1 = Vx/Vin	   	   and	  Av2 = Vout/Vx
  * Open Loop Gain = Av = Av1 x Av2

* Power = 8mW
* Vdd = 3.3V
* Id = 8mW/3.3V = 2.424242 mA

![alt text](https://github.com/nikhil1198/2-Stage-Operational-Amplifier/blob/master/calc.JPG)

# LTSpice Simulation Results:
* Input:

![alt text](https://github.com/nikhil1198/2-Stage-Operational-Amplifier/blob/master/input.JPG)

* Operation Point Analysis:

![alt text](https://github.com/nikhil1198/2-Stage-Operational-Amplifier/blob/master/op1.JPG)

![alt text](https://github.com/nikhil1198/2-Stage-Operational-Amplifier/blob/master/op2.JPG)

* Frequency Response: 

![alt text](https://github.com/nikhil1198/2-Stage-Operational-Amplifier/blob/master/out123.JPG)

 * The frequency response (Bode Plot curve) of the two stage op amp simulated is similar to a single pole one stage op amp in the required bandwidth (operation region)
 * The second pole occurs at 800MHz(P2=gm6/Cl , approx.) which in insignificant to our amplifier operation.
 * The only zero occurring at Z1=gm6/Cc  because of Miller capacitor introduced(Cc) is at 1.25 GHz(approx.) which is also insignificant to our operation.
 * Hence the Bode plot is as shown and is equivalent to a one pole system till a few hundred MHz  (until we have significant gain)
 
# Conclusion:

* A common “workhorse” opamp for medium performance applications.
* A reasonably simple structure with reasonable performance
* Design issues introduced : Two poles close to each other introduced. Very poor phase margin and instability until high load capacitance used.
* Hence, the Concept of pole splitting introduced to decrease (shift left ) the dominant pole frequency which introduced because of stage one, causing stability

# Summary:

* A two stage OpAmp is designed with the given specifications. 
* First, a hand design was done followed by simulation in LTspice IV. The results are in agreement with the required value with a very small trade-off.
* The trade-off may be due to neglecting body effect or any other transistor in built properties.






