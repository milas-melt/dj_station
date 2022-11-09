This project consists of a small, portable DJ mixer powered by a 9V dc external supply adaptor or from a 9V PP3 battery. The mixer features two stereo phono inputs and two stereo line-level inputs and has one stereo mixing channel. A microphone input and a stereo main output with adjustable gain are also provided. Headphone monitoring includes a cue switch for selecting Channel 1, Channel 2 or Master Channel. For easy understanding, the circuit is divided into five blocks, as follows:

-   General Circuit diagram:
    All passive circuitry (controls, faders, switches, input and output connectors) is shown in full, whereas active amplification modules are represented by suitably labeled triangle symbols.
-   Phono Amplifier Module:
    A high gain stereo amplifier suitable for moving magnet pick-up cartridges, having a frequency response according to RIAA equalization curve and based on the low noise, low distortion LS4558 dual IC. Two identical stereo modules of this type are required.
-   Microphone Amplifier Module:
    A single transistor, low noise, high gain microphone amplifier, suitable for low impedance microphones.
-   Mixer Module:
    A stereo circuit incorporating two virtual-earth mixers based on the dual BIFET TL062 Op-Amp.
-   Headphone Amplifier Module:
    This circuit was already present on this website under Portable 9V Headphone Amplifier. It features a low current drain stereo amplifier based on the low distortion, low noise 5532 dual IC, capable of delivering 3.6V peak-to-peak into 32 Ohm load at 9V supply (corresponding to 50mW RMS) with less than 0.025% total harmonic distortion (1kHz & 10kHz).

# General Circuit Diagram:

## DJ Station General Circuit diagram

![DJ Station General Circuit diagram](https://github.com/milas-melt/dj_station/blob/master/images/general_circuit_diagram.gif)

## Parts:

- P1,P2,P4,P5: 22K Dual gang Log Potentiometers
- : P3: 22K Dual gang Linear Potentiometer
- P6: 22K Log Potentiometer
- R1 to R10: 30K 1/4W 1% or 2% tolerance Resistors
- R11: 1K 1/4W Resistor
- C1: 2200µF 25V Electrolytic Capacitor
- D1: 3mm. or 6mm. red LED
- J1 to J10: RCA audio input sockets
- J11: 6mm. or 3.5mm. Stereo Jack socket
- J12: 6mm. or 3.5mm. Mono Jack socket
- J13: Mini DC Power Socket
- SW1,SW2: DPDT toggle or slide Switches
- SW3: 2 poles 3 ways Rotary Switch
- SW4: SPST toggle or slide Switch

## Circuit description:

The input source can be selected by means of SW1 for Channel 1 and SW2 for Channel 2. Moving magnet pick-ups must be connected to Phono 1 and 2 inputs, whereas CD players, iPods, Tape recorders, PC Audio outputs and the like can be connected to Line 1 and 2 inputs. After a separate Level control for each channel (P1 and P2), the two incoming audio signals are mixed and cross-faded by means of P3 and associated resistors network. The Crossfader control mixes both Channels at the same intensity when set in the middle position. When the cursor of P3 is fully rotated towards R3-R4, only Channel 1 signal is present at the Main output, whereas Channel 2 is muted.

Conversely, Channel 2 signal is present at the Main output and Channel 1 is muted when the cursor of P3 is fully rotated towards R1-R2. This network is followed by the Mixer Amplifier, the Master Level P4 and the Main output sockets. A low impedance microphone can be connected to the Mic input. P6 controls the signal level after amplification by the Microphone Amplifier module and feeds the Left and Right Mixer Amplifiers through R9-R10. In this way, the speaker's voice will be reproduced at the center of the soundstage.

A stereo Headphone Amplifier with cue gain control is provided for monitoring purposes. The Cue Select switch SW3 will allow Headphone reproduction of Channel 1, Channel 2 or Master Channel, independently of the signal present at the Main Output. J13 is a Mini DC Power Socket into which the suitable plug of a 9V dc external supply adaptor should be inserted. In any case, due to the low total current drain (about 13mA average), a 9V battery can be used satisfactorily to power the entire Station.

# Magnetic Pick-up Amplifier Module

## Magnetic Pick-up Amplifier Circuit Diagram

![Magnetic Pick-up Amplifier Circuit Diagram](https://github.com/milas-melt/dj_station/blob/master/images/headphone_amplifier_module.gif)

## Parts:

- R1,R10: 2K2 1/4W Resistors
- R2,R3,R11,R12: 100K 1/4W Resistors
- R4,R13: 1K 1/4W Resistors
- R5,R6,R14,R15: 18K 1/4W Resistors
- R7,R16: 390K 1/4W Resistors
- R8: 220R 1/4W Resistor
- R9,R17: 10K 1/4W Resistors
- C1,C5,C6,C10: 22µF 25V Electrolytic Capacitors
- C2,C7: 47µF 25V Electrolytic Capacitors
- C3,C8: 2n2 63V Polyester or Polystyrene low tolerance Capacitors
- C4,C9: 10nF 63V Polyester or Polystyrene low tolerance Capacitors
- C11: 100µF 25V Electrolytic Capacitor
- IC1: LS4558 Dual High Performance Op-Amp

## Circuit description:

A straightforward series-feedback amplifier circuit with RIAA frequency compensation, based on the High Performance LS4558 Op-Amp was used for this stage.
Despite the low supply voltage operation, the performance of this Circuit Module is quite good.

## Note:

Two identical stereo modules of this type are required.
A more strict RIAA equalization curve will be obtained if low tolerance components are used for R5, R6, R7, R14, R15, R16 (1% - 2%) and C3, C4, C8, C9 (2% - 5%).

# Microphone Amplifier Module

## Microphone Amplifier Circuit Diagram

![Microphone Amplifier Circuit Diagram](https://github.com/milas-melt/dj_station/blob/master/images/magnetic_pickup_amplifier_module.gif)

## Parts:

- R1: 1M2 1/4W Resistor
- R2: 5K6 1/4W Resistor
- R3: 1K 1/4W Resistor
- C1,C3: 4µ7 63V Electrolytic Capacitors
- C2: 100µF 25V Electrolytic Capacitor
- Q1: BC550C 45V 100mA Low noise High gain NPN

## Circuit description:

This circuit module, based on a very simple, single transistor amplifier, features a low noise, 45dB stage gain. Input impedance: 2700 Ohm.

# Mixer Module

## Mixer Circuit Diagram

![Mixer Circuit Diagram](https://github.com/milas-melt/dj_station/blob/master/images/microphone_amplifier_module.gif)

## Parts:

- R1,R2: 68K 1/4W Resistors
- R3,R4: 120K 1/4W Resistors
- C1,C2,C4,C6,C8: 4µ7 63V Electrolytic Capacitors
- C3,C7: 10pF 63V Ceramic Capacitors
- C5: 100µF 25V Electrolytic Capacitor
- IC1: TL062 Low current BIFET Dual Op-Amp

## Circuit description:

Straightforward virtual-earth mixer-amplifier stage based on the very low current drawing BIFET TL062 Op-Amp.

# Headphone Amplifier Module:

## Headphone Amplifier Circuit Diagram

![Headphone Amplifier Circuit Diagram](https://github.com/milas-melt/dj_station/blob/master/images/mixer_module.png)

## Parts:

- R1,R5: 18K 1/4W Resistors
- R2,R3,R4,R6: 68K 1/4W Resistors
- C1,C2,C6: 4µ7 25V Electrolytic Capacitors
- C3,C7: 22pF 50V Ceramic Capacitors
- C4,C5,C8: 220µF 25V Electrolytic Capacitors
- IC1: NE5532 Low noise Dual Op-amp

## Circuit description:

For a complete description of this stage see: Portable 9V Headphone Amplifier.

## Technical data:

### Sensitivity:

Microphone Input: 3.5mV RMS
Phono Input: 8mV RMS
Line Input: 500mV RMS

### Maximum undistorted output:

Main output: 2.5V RMS
Headphones: 1.27V RMS into 32 Ohm load

### Frequency response:

Microphone and Line: flat from 20Hz to 20KHz
Phono: according to RIAA curve ±1dB
Headphones: flat from 40Hz to 20KHz; -2.3dB @ 20Hz

### Total harmonic distortion @ 1KHz and 1V RMS output:

Line: 0.013%
Phono: 0.016%
Headphones: 0.025%

### Total current drawing @ 9V supply:

Standing current: 10mA
Mean current drawing: 13mA

reference: https://www.learningelectronics.net/
