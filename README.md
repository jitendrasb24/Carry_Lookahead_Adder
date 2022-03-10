# 4_Bit_Carry_Lookahead_Adder
This repository presents the design of 4 bit Carry Lookahead Adder implemented using eSim.

## ABSTRACT
A Carry Lookahead Adder is proposed in this paper.
Design and Implementation is done using eSim Software. The
Carry Lookahead Adder has a significant role in modern systems
where speed and time reduction are of major priority. We can
verify the output using Circuit Waveforms.

## TOOLS USED
* **Esim**

## INTRODUCTION
Carry Lookahead Adder (CLA) is superior than full adder
(in terms of speed). It is also known as parallel adder. It
takes advantage of computational parallelization at the cost
of increased complexity and power consumption. This parallelization benefits decrease in propagation time. In normal
Full Adder each output sum bit needs to wait until the previous
carry bit have been calculated. But in CLA, all carry bits are
calculated before calculating sum bits which reduce the wait
time. One of the most important efficiency of CLA is to predict
the carry before it’s actually calculated. Transistor size is also
selected based upon simulation and optimization, to reach the
needed performance according to the cost function.

## CIRCUIT DETAILS
Here we are designing 4-bit CLA process by using conventional static CMOS. The power supply is varied from 1.0
Volts to 2.8 Volts for proposed and basic design. The proposed
circuit will be implemented in eSim EDA tool. In circuit, basic element
is NMOS and PMOS is used to made every block. Two
intermediate terms, called propagate and generate bits are used
to calculate sum (S) and carry out (Cout) bits. If we define two
variables as carry generate Gi and carry propagate Pi then, Pi
= Ai xor Bi; Gi = Ai and Bi; The sum output and carry output
can be expressed as Si = Pi xor Ci; Ci + 1 = Gi or (Pi and
Ci); Where Gi is a carry generate which produces the carry
when both Ai, Bi are one regardless of the input carry. Pi is
a carry propagate and it is associate with the propagation of
carry from C1 to Ci +1 (Because input carry is already is given
with Ai and Bi). I was able to reach a 4-bit ripple carry adder
that has delay of 1.22 ns with 0.6 uW power consumption
(measured at 10 MHz), with 200 mosfets. Every carry bit can
be found from the generate and propagate terms. Once the
carry-out bits have been calculated, the sums are found using
the simple XOR operation. Carry Look Ahead Adder (CLA)
uses direct parallel-prefix scheme for carry computation. Its
time delay(T) and area complexity(A) are as follows for an
n-bit CLA adder: T = (2log(n) + 4); A = ((3/2)nlog(n) + 4n + 5). And also n bit cla cost will be = 7n +(1/6)n(n+1)(n+5).

## CIRCUIT SCHEMATIC
![Circuit](https://user-images.githubusercontent.com/86667690/157678479-84825f1f-d764-445a-9968-32375191f6f2.jpg)


## CIRCUIT WAVEFORMS

![waveform](https://user-images.githubusercontent.com/86667690/157678152-b6649232-461f-462b-8952-3c4ac7bd2e64.jpg)


![waveform1](https://user-images.githubusercontent.com/86667690/157678100-9e4ce7d4-7427-4ec7-9065-92e1a50d414a.jpg)

## AUTHOR

**JITENDRA SINGH BISHT**

**Bachelor of Technology(B.TECH)**

**3rd year Student**

**Bipin Tripathi Kumaon Institute of Technology, Dwarahat**


## ACKNOWLEDGEMENT

1. Mixed Signal Design Hackathon
2. FOSSEE
3. IIT Bombay
4. VLSI System Design (VSD) Corp. Pvt. Ltd India
5. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.
6. Sumanto Kar, IIT Bombay

## REFERENCES

1. M. Morris Mano, Michael D. Ciletti, Digital Design Book, 6 Edition, By Pearson.
2. https://en.wikipedia.org/wiki/Carry-lookahead adder.
3. M. Hasan. High-performance design of a 4-bit carry look-ahead adder in static cmos logic. http://section.iaesonline.com/index.php/IJEEI/article/view/2582.
4. I. S. Dhanjal, 4 bit carry look ahead adder transistor level implementation using static cmos logic. https://youtu.be/WItAXzrfPrE.


