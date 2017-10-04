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





