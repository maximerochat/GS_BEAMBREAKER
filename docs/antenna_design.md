# Antenna

<!-- TOC -->
* [Antenna](#antenna)
  * [Mathematics](#mathematics-)
  * [Production](#production)
<!-- TOC -->


The Antennas are a big part of this project since they are the last physical layer that interact with our system.

After some initial research about beam-forming, I noticed that they were all usually using small patch antenna tuned for
their frequency of action. So that will be my choice in this project since in addition to that it seems pretty easy to
produce and well documented. 

## Mathematics 
After looking at some research paper and browsing on the net I found a perfect [blog post](https://resources.altium.com/fr/p/microstrip-patch-antenna-calculator-rf-designers) on the altium website
that features a complete calculator for patch antenna. You can find required ressource here and for a first throw I found get 
the following result for the sizing of my antenna : 

| Edge  | length(mm) |
|:-----:|:----------:|
|   L   |    27.7    |
|   W   |     36     |
|   D   |    7.9     |
|   S   |    0.51    |
|  W0   |    0.34    |
| A     |    6.9     |

using FR4 as dielectric material that as a ε ≈ 4.7, h=0.2mm which is a common height between plane for 4 layer PCB's 
and centered at f=2.4GHz. The calculator include the impedance of the antenna is design to be around 50 Ohms which is the 
default impedance for most RF systems as far as I know.

// TODO  put a scheme of the different width 

## Production
The advantage of the patch antenna is that it's pretty easy to produce and to print on a PCB since it's basicly 
just a copper plane over a ground plane (or at least it's what I think;). I'll try to add some image of kicad design when 
I'll have finished to design them.

// TODO add photos of kicad    