# Hardware

In this section, we'll talk about hardware related question. 

# Table of content
- [Radio module](#radio-module)
- [Power Splitter](#power-splitter)
- [Phase Shifter](#phase-shifter)
- [Amplifier](#amplifier)


# Radio module
For the radio module, I will use the [Semtech SX1280](https://www.tme.eu/Document/1042f35a88b6ee421559d19923804032/SX128x.pdf), that is a very polyvalent radio module that has capabilities to manage
different type of modulation at pretty high bit rate in 2.4GHz. In this project I'll try to design it to and FSK at 2MBit/s. 

# Power Splitter
In order to interface the signal from the single output of the radio transceiver and the 2x2 patch antenna front-end, we
will need to use a power divider that will divide our RF trace into 4 separate traces for each antenna. To achieve this I found the 
[MAPDCC0010](https://www.mouser.ch/datasheet/2/249/MAPDCC0010-318460.pdf) that has the required specification.


# Phase shifter 
On of the most important component to achieve beam steering is the phase shifter since 
it is this tiny component that can control out phase shift to direct the beam. The most challenging part
is to find one that suits our need and that is not to expensive. 

There seems to be really good product from Analog Devices but they are to expensive for my project at this time, that's why 
i would choose (for my first iterations at least) an alternative, the [PS214-315](https://mm.digikey.com/Volume0/opasdata/d220001/medias/docus/581/PS214-315.pdf).

The main drawback of this product is that it as only a shift range on ~100° at 2.4GHz which means we won't be able to fully steer the beam as we wish,
but it is certainly sufficient for the beginning.

# Amplifier
After the power splitter and to ensure good signal strength we need an amplifier. After some research i found the [SKY65405-21](https://www.mouser.ch/datasheet/2/472/SKY65405_21_201446I-3364501.pdf) that seemed to fit all my requirements.

