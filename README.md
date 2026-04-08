# 📡 Design and Implementation of an International Digital Terrestrial TV Receiver using an FPGA

Report
[Document (docx format)](https://github.com/vahejab/DTV-Receiver/blob/main/ECE-699C-Final-Report-Final-Version.dodx)


**Author:** Vahe Robert Jabagchourian  
**Course:** ECE 699C – Independent Study  
**Instructor:** Professor Ronald Mehler  
**Institution:** California State University, Northridge  
**Date:** November 24, 2008  

---

# 📑 Table of Contents

- [1. Project Objective](#1-project-objective)
- [1.1 Digital TV Background](#11-digital-tv-background)
- [1.2 Benefits of Digital TV](#12-benefits-of-digital-tv)
- [1.3 Software Defined Radio](#13-software-defined-radio)
- [1.4 Project Breakdown](#14-project-breakdown)
- [2. Terrestrial Modulation Methods](#2-terrestrial-modulation-methods)
- [3. Characteristics of Digital TV Standards](#3-characteristics-of-digital-tv-standards)
- [4. Compatibility of the Standards](#4-compatibility-of-the-standards)
- [5. Summary](#5-summary)
- [6. Conclusion](#6-conclusion)

---

# 1. Project Objective

The purpose of this project is to design, test and implement a Digital TV receiver that can receive standards from across the world using software defined routines and an FPGA (Field Programmable Gate Array).

Throughout this document we will study the feasibility of implementing a Digital Terrestrial Television (DTTV) receiver module using a Field Programmable Gate Array, and a front end Analog to Digital Converter (ADC) to directly quantize the Radio Frequency (RF) signal and analog front end components for signal acquisition.

---

## 📷 Figure 1.1 – Overview of Digital TV Receiver

![Figure 1.1](https://github.com/vahejab/DTV-Receiver/blob/main/image_1.png)

## 📷 Figure 1.2 – Global Coverage of Digital Terrestrial TV Standards

![Figure 1.2](https://github.com/vahejab/DTV-Receiver/blob/main/image_2.png)

---

# 1.1 Digital TV Background

Digital TV is a TV standard that allows transmission and reception of moving images (specifically MPEG Streams) digitally (in a binary number system).

Though the actual Radio Frequency signals may be in analog format, the data that is in those analog signals is interpreted in a digital representation.

Digital TV is more flexible and efficient than analog television.

The primary difference between digital and analog TV is that digital TV is capable of producing higher quality images, sound and provides more programming choices than analog TV.

---

# 1.2 Benefits of Digital TV

A. The main reason that terrestrial TV will transition to digital is that the frequencies allocated for certain analog channels need to be reallocated for other public services such as wireless, and police and firefighting communications.

B. Many TV stations are spending money transmitting to consumers both in an analog format and digital, that is until February 19, 2009 when all analog transmission in the US will switch to digital.

C. Digital is much less susceptible to noise and can provide a near perfect reproduction of the source image at a far greater image quality.

D. Digital spectrum is far more efficient in its usage.

---

## 📷 Figure 1.3 – ATSC and NTSC Channel Spectrum Comparison

![Figure 1.3](https://github.com/vahejab/DTV-Receiver/blob/main/image_3.png)

---

# 1.3 Software Defined Radio

Software Defined Radio is a Radio System that implements most of the functions traditionally realized through hardware in software.

Mixers, filters, modulators are implemented using FPGA devices where as traditional devices use physical components that are fixed.

The major device in SDR is the analog to digital converter which is placed close enough to the receiver antenna so that the majority of the software can be put right after the A/D conversion.

True SDR is difficult to realize due to current technological limits.

---

## 📷 Figure 1.4 – True Software Defined Radio Block Diagram

![Figure 1.4](https://github.com/vahejab/DTV-Receiver/blob/main/image_4.png)

## 📷 Figure 1.5 – SDR Infrastructure

![Figure 1.5](https://github.com/vahejab/DTV-Receiver/blob/main/image_5.png)

## 📷 Figure 1.6 – Simplified Front End Receiver

![Figure 1.6](https://github.com/vahejab/DTV-Receiver/blob/main/image_6.png)

---

# 1.4 Project Breakdown

## A. RF Front End

Digital TV is transmitted between 470 MHz – 770 MHz in Ultra High Frequency (UHF).

The Band Pass Filter removes unwanted frequencies and the Variable Gain Amplifier stabilizes signal amplitude.

---

## B. Analog to Digital Conversion

Nyquist criteria requires sampling at twice the highest frequency.

This results in a required sampling rate of approximately 1.6–2.0 GSPS.

---

## C. Digital Down Conversion

## 📷 Figure 1.7 – Digital Down Converter Block

![Figure 1.7](https://github.com/vahejab/DTV-Receiver/blob/main/image_7.png)

---

## D. Demodulation

Each standard has its own demodulation scheme.

## 📷 Figure 1.8 – Region Specific Demodulator

![Figure 1.8](https://github.com/vahejab/DTV-Receiver/blob/main/image_8.png)

---

## E. Error Correction

## 📷 Figure 1.9 – Error Correction Blocks

![Figure 1.9](https://github.com/vahejab/DTV-Receiver/blob/main/image_9.png)

---

# 2. Terrestrial Modulation Methods

## 2.1 Fundamentals of Amplitude Modulation

Amplitude modulation varies the amplitude of a carrier signal.

---

## 2.2 8-VSB

## 📷 Figure 2.1 – 8VSB Signal

![Figure 2.1](https://github.com/vahejab/DTV-Receiver/blob/main/image_10.png)

---

## 2.3 Frequency Division Multiplexing

## 📷 Figure 2.2 – FDM

![Figure 2.2](https://github.com/vahejab/DTV-Receiver/blob/main/image_11.png)

---

## 2.4 Orthogonal Frequency Division Multiplexing

## 📷 Figure 2.3 – OFDM

![Figure 2.3](https://github.com/vahejab/DTV-Receiver/blob/main/image_12.png)

---

## 2.5 Quadrature Amplitude Modulation

## 📷 Figure 2.4 – QAM Constellation

![Figure 2.4](https://github.com/vahejab/DTV-Receiver/blob/main/image_13.png)

---

# 3. Characteristics of Digital TV Standards

## 3.1 ATSC

![Figure 3.1](https://github.com/vahejab/DTV-Receiver/blob/main/image_14.png)  
![Figure 3.2](https://github.com/vahejab/DTV-Receiver/blob/main/image_15.png)  
![Figure 3.3](https://github.com/vahejab/DTV-Receiver/blob/main/image_16.png)  
![Figure 3.4](https://github.com/vahejab/DTV-Receiver/blob/main/image_17.png)  
![Figure 3.5](https://github.com/vahejab/DTV-Receiver/blob/main/image_18.png)

---

## 3.2 DVB-T

![Figure 3.6](https://github.com/vahejab/DTV-Receiver/blob/main/image_19.png)

---

## 3.3 ISDB-T

![Figure 3.8](https://github.com/vahejab/DTV-Receiver/blob/main/image_20.png)

---

## 3.4 DTMB

![Figure 3.9](https://github.com/vahejab/DTV-Receiver/blob/main/image_21.png)

---

# 4. Compatibility of the Standards

All standards operate in similar frequency bands but differ in:

- Modulation techniques  
- Error correction  
- Carrier structure  

---

## 📷 Demodulation Figures

![Figure 4.1](https://github.com/vahejab/DTV-Receiver/blob/main/image_22.png)  
![Figure 4.2](https://github.com/vahejab/DTV-Receiver/blob/main/image_23.png)

---

# 5. Summary

All four standards:

- Use MPEG transport streams  
- Operate in UHF  
- Use forward error correction  

---

# 6. Conclusion

The recommended approach is:

- FPGA for real-time DSP  
- Software for flexible decoding  

This hybrid system ensures performance and adaptability.

---

# 📚 References

1. **"ATSC transmission."** Broadcast Engineering, 20 June 2005.  
   Available: http://broadcastengineering.com/infrastructure/Atsc-transmission-digital-20050620/

2. **"Digital Multimedia Broadcasting."** Wikipedia, 2008.

3. **"Figure 12: Bandwidth Allocations for an FDM Communications System."**  
   National Instruments, 2 January 2007.  
   Available: http://zone.ni.com/devzone/cda/tut/p/id/3876

4. **"Modulation."** Wikipedia.  
   Available: http://en.wikipedia.org/wiki/Modulation

5. **"Pulse-Shape Filtering in Communications Systems."**  
   National Instruments.  
   Available: http://zone.ni.com/devzone/cda/tut/p/id/3876

6. **"What Exactly is ATSC?"** HDTV Primer.  
   Available: http://www.hdtvprimer.com/ISSUES/what_is_ATSC.html

7. **Andraka, Ray.**  
   *"Modulation and Demodulation Techniques for FPGAs."*  
   DesignCon 2000.  
   Available: http://www.andraka.com/files/designcon00.pdf

8. **Barnes, Kai.**  
   *"Multiantenna SDR Architectures and its Simplification Methods."*  
   Centre for Wireless Communications, 2005.  
   Available: http://www.cwc.oulu.fi/home/coursedata/softwareradios_juntti/SDR_arch.pdf

9. **Cugnini, Aldo.**  
   *"World TV Standards."* Broadcast Engineering, October 2007.  
   Available: http://broadcastengineering.com/hdtv/world_tv_standards/

10. **Dick, Chris.**  
    *"Design and Implementation of High-Performance FPGA Signal Processing Datapaths for Software Defined Radios."*  
    Xilinx Inc.  
    Available: http://www.xilinx.com/esp/mil_aero/collateral/ProductEngineering/design_implementaion.pdf

11. **Francis, Michael.**  
    *"Forward Error Correction in Digital Television Broadcast Systems."*  
    Xilinx, April 2008.  
    Available: http://www.xilinx.com/support/documentation/white_papers/wp270.pdf

12. **Gray, Robert.**  
    *"Costas Loop, Noise in AM, SSB/VSB. AM Radio and Superheterodyne Receivers."*  
    Stanford University.  
    Available: http://www.stanford.edu/class/ee179/summaries/lecture19.pdf

13. **Jack, Keith.**  
    *Video Demystified*, 4th Edition.  
    Burlington: Newnes, 2004.

14. **Ladebusch, Uwe.**  
    *"Terrestrial DVB (DVB-T): A Broadcast Technology for Stationary Portable and Mobile Use."*  
    Proceedings of the IEEE, Vol. 94, 2006.

15. **Miller, William.**  
    *"Chapter 9: DTV Test, Measurement and Monitoring."*  
    *The Guide to Digital Television*, Third Edition, 2000.  
    Available: http://www.thevideoguru.com/dtvbook/ch9.html

16. **Oyamada, Kimiyuki.**  
    *"ISDB-C - Cable Television Transmission for Digital Broadcasting in Japan."*  
    Asia-Pacific Broadcasting Union, 2001.  
    Available: http://www.nhk.or.jp/strl/publica/bt/en/pa0007.html

17. **Sparano, David.**  
    *"What Exactly is 8-VSB Anyway?"*  
    Harris Corporation Broadcast Division, August 2002.  
    Available: http://www.8vsb.com/WhatExactlyIs.htm

18. **Tuğcu, Tuna.**  
    *"Cognitive Radio."*  
    Available: http://www.cmpe.boun.edu.tr/~tugcu/research.html#Cognitive_Radio

19. **Yokohata, Kazunori.**  
    *"ISDB-T Transmission Technology - Single Transmission for Fixed, Vehicular, and Handheld Receivers."*  
    Available: http://ru.ictp.uz/summit2007/yokohata.pdf
