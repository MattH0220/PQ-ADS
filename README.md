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
1. **Literature Study and Requirements Definition**  
   Conducted a comprehensive review of PocketQube satellites and existing antenna deployment systems to establish design requirements. Defined specifications for the ADS, including PQ9 standard compliance (42x42 mm PCB), reliable deployment, and efficient RF performance for TT&C communication.  
   ![Literature Study Placeholder](https://via.placeholder.com/600x400?text=Insert+Literature+Study+Image)

2. **System Design Overview**  
   Developed a high-level design of the SUNQube-1 communication system, focusing on the ADS’s role in enabling bidirectional data relay. Designed subsystems including a half-wavelength dipole antenna, deployment mechanism, and detection system, ensuring integration with the satellite’s On-Board Computer (OBC) and Electrical Power System (EPS).  
   ![System Design Placeholder](https://via.placeholder.com/600x400?text=Insert+System+Design+Image)

3. **RF Design and Antenna Configuration**  
   Selected UHF (433 MHz) for smaller antenna size and reduced interference. Designed a half-wavelength dipole antenna with an L-network for impedance matching to achieve a 50Ω target, minimizing reflection losses. Addressed challenges of feeding a balanced antenna with an unbalanced coaxial cable.  
   ![RF Design Placeholder](https://via.placeholder.com/600x400?text=Insert+RF+Design+Image)

4. **Mechanical Design of Deployment Mechanism**  
   Designed a compact deployment mechanism using a burn-wire and thermal knife system with a coiled antenna storage system. Incorporated a 3D-printed mounting block and conductive copper tape for electrical connections, ensuring compliance with PQ9 size constraints and LEO environmental challenges.  
   ![Mechanical Design Placeholder](https://via.placeholder.com/600x400?text=Insert+Mechanical+Design+Image)

5. **Electrical Design and Deployment Detection**  
   Developed the electrical subsystem, including a burn subsystem powered by a 5V EPS supply and a deployment detection subsystem using a GP2S700HCP reflective photointerrupter. Integrated a comparator circuit to convert analog sensor signals to digital for OBC interfacing, optimizing power efficiency.  
   ![Electrical Design Placeholder](https://via.placeholder.com/600x400?text=Insert+Electrical+Design+Image)

6. **Prototype Development and Integration**  
   Built a Minimum Viable Product (MVP) to test mechanical functionality, identifying and resolving a clearance issue in the burn-wire attachment. Integrated all subsystems onto a single PCB, optimizing component placement for signal integrity and structural stability.  
   ![Prototype Placeholder](https://via.placeholder.com/600x400?text=Insert+Prototype+Image)

7. **Testing and Validation**  
   Conducted extensive testing, including thermal tests on the burn resistor (achieving wire cutting at 87°C), deployment tests to verify mechanical reliability, and RF tests to measure impedance, VSWR, and S11 parameters. Compared matched and unmatched antenna performance, confirming the matched antenna’s superior results (VSWR of 1.2001 and return loss of -20.67 dB).  
   ![Testing Placeholder](https://via.placeholder.com/600x400?text=Insert+Testing+Image)

8. **Full System Functional Test**  
   Performed a full system test with the TT&C radio board using an SX1278 transceiver configured for GFSK modulation. Validated data packet transmission against a commercial monopole antenna, confirming the matched antenna’s comparable or superior performance.  
   ![Full System Test Placeholder](https://via.placeholder.com/600x400?text=Insert+Full+System+Test+Image)

9. **Documentation and Future Work**  
   Documented the design, testing, and results in a comprehensive thesis, proposing a balun to address RF ground plane resonance issues. Suggested future enhancements, such as advanced antenna technologies and further miniaturization, for broader PocketQube applications.  
   ![Documentation Placeholder](https://via.placeholder.com/600x400?text=Insert+Documentation+Image)
