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


