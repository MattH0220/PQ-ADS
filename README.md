# PQ-ADS

## Overview
The PQ-ADS project focuses on the design, development, and testing of a compact Antenna Deployment System (ADS) for the SUNQube-1, a student-built PocketQube satellite developed at Stellenbosch University. PocketQubes are a class of pico-satellites, typically measuring 5x5x5 cm per unit (1P), designed to provide cost-effective access to space for small institutions. The ADS integrates a half-wavelength dipole antenna, a reliable deployment mechanism, and a deployment detection subsystem onto a single custom PCB, adhering to the stringent PQ9 standard size constraints. The system ensures reliable telemetry, tracking, and command (TT&C) communication for the SUNQube-1 mission while being adaptable for future PocketQube missions. The ADS demonstrated successful deployment and data transmission.


<table align="center">
  <tr>
    <td>
      <img width="400" height="240" alt="image" src="https://github.com/user-attachments/assets/ce62e537-46a1-46be-bcda-629fac5a99c6" />
    </td>
  </tr>
</table>

## Objective
The primary objective of the PQ-ADS project was to design and develop a compact, reliable Antenna Deployment System (ADS) for the SUNQube-1 PocketQube satellite mission, ensuring compliance with the PQ9 standard. The project aimed to integrate a half-wavelength dipole antenna, a deployment mechanism, and a deployment detection subsystem onto a single PCB, optimizing for size, reliability, and functionality. Key goals included achieving efficient RF performance through impedance matching, ensuring reliable antenna deployment in orbit, and validating the system’s ability to transmit TT&C data packets, creating a versatile solution for future PocketQube missions.

### Skills Learned
- Antenna design and RF engineering, including impedance matching and antenna configuration for UHF frequencies.
- Mechanical design of compact deployment mechanisms tailored for space applications.
- PCB design and layout, ensuring signal integrity and compatibility with PQ9 standards.
- Embedded systems programming for deployment control and detection using microcontrollers.
- Independent learning and application of CAD and PCB design software for system development.
- Rigorous testing and validation techniques, including thermal, mechanical, and RF performance testing.
- Problem-solving and iterative design to address mechanical and RF challenges in a space environment.
- Project management and documentation for a complex engineering project.

### Tools Used
- OnShape CAD software.
- KiCAD for PCB design and layout.
- Vector Network Analyzer (VNA).
- Multimeter and thermocouple.
- ESP32 microcontroller.
- ST-Link dongle and UART-to-serial dongle for programming and debugging the TT&C radio board.
- Termite software.
- Benchtop power supplies.

## Steps
1. **RF Design and Antenna Configuration**  
   Selected UHF (433 MHz) for smaller antenna size and reduced interference. Designed a half-wavelength dipole antenna with an L-network for impedance matching to achieve a 50Ω target impedance, minimizing reflection losses. I used a smith chart to determine the L and C values that would transform the dipole antennas 73Ω to the desired 50Ω.

<table align="center">
  <tr>
    <td>
      <img width="564" height="219" alt="image" src="https://github.com/user-attachments/assets/08889754-fbac-42ba-8ff7-b959ae0d0ca5" />
    </td>
  </tr>
</table>


2. **Mechanical Design of Deployment Mechanism**  
   Designed a compact deployment mechanism using a burn-wire and thermal knife system with a coiled antenna storage system. Incorporated a 3D-printed mounting block and conductive copper tape for electrical connection of the antenna elements, ensuring compliance with PQ9 size constraints and LEO environmental challenges.  
   
<table align="center">
  <tr>
    <td>
      <img width="693" height="219" alt="image" src="https://github.com/user-attachments/assets/037d8f8c-effe-4ec5-a8b5-ca5b9da4ec8a" />
    </td>
  </tr>
</table>


3. **Electrical Design and Deployment Detection**  
   Developed the electrical subsystem, including a burn subsystem powered by a 5V supply (that required a logic level shifting circuit, to allow the 3.3v OBC signal to switch the 5V), a deployment detection subsystem using a GP2S700HCP reflective photointerrupter, which I positioed in a cutout in the antenna deployment door as shown in the 3D render below. The deployment detection circuit is used to cut power to the burn resistor once successful deployment has occured, saving power. I also integrated a comparator circuit to convert the analog signals from the GP2S700HCP to digital for OBC interfacing.  
   
<table align="center">
  <tr>
    <td>
      <img width="823" height="219" alt="image" src="https://github.com/user-attachments/assets/f1b177b9-e1d0-4ce0-ac5a-62cb23ef5c62" />
    </td>
  </tr>
</table>


4. **Subsystem Integration and PCB Design**  
   Integrated all subsystems onto a single PCB, optimizing component placement for signal integrity and structural stability. The figure below illustrates the fuller assembled top and bottom view of the PCB.  
<table align="center">
  <tr>
    <td>
      <img width="712" height="218" alt="image" src="https://github.com/user-attachments/assets/fef0e2b5-af86-4704-b6a5-91c4b5a201f1" />
    </td>
  </tr>
</table>

5. **Testing and Validation**  
   Conducted extensive testing, including deployment tests to verify mechanical reliability, and RF tests to measure impedance, VSWR, and S11 parameters. Compared matched and unmatched antenna performance, confirming the matched antenna’s results (VSWR of 1.2001 and return loss of -20.67 dB).  
<table align="center">
  <tr>
    <td>
      <img width="690" height="254" alt="image" src="https://github.com/user-attachments/assets/f2d08d21-c9a7-4502-82c7-c278c87ff803" />
    </td>
  </tr>
</table>

<table align="center">
  <tr>
    <td>
      <img width="800" height="500" alt="image" src="https://github.com/user-attachments/assets/513347e3-5cc4-4826-a256-469558c234f0" />
    </td>
  </tr>
</table>

6. **Full System Functional Test**  
   Performed a full system test with the TT&C radio board using an SX1278 transceiver configured for GFSK modulation. Validated data packet transmission against a commercial monopole antenna, confirming the matched antenna’s comparable or superior performance.  
   
<table align="center">
  <tr>
    <td>
      <img width="663" height="124" alt="image" src="https://github.com/user-attachments/assets/2eccbb3b-2ae7-44ea-8a05-0a78d8c4bf81" />
    </td>
  </tr>
</table>


