# ACOMP01 - Fast Analog Comparator Module

The ACOMP01 module is a high-speed dual comparator board with differential LVDS outputs. It is designed for fast signal discrimination in nanosecond-scale timing systems. Each comparator features coaxial MCX input connectors and differential output for integration into high-speed digital acquisition or timing logic circuits.

![ACOMP01 top view](/doc/gen/img/ACOMP01-top.png) ![ACOMP01 bottom view](/doc/gen/img/ACOMP01-bottom.png)

## Typical Applications

- High-speed pulse discrimination
- Oscilloscope triggering
- LIDAR and ToF sensing
- Nuclear and particle physics detectors
- Time interval measurement systems

## Features

- Two independent comparator channels
- High-speed response with sub-nanosecond propagation delay
- Differential LVDS outputs
- MCX connectors for analog input signals
- Designed for precise pulse timing and triggering

## Comparators Used

### TLV3604
- Propagation delay: 800 ps
- Toggle rate: up to 3 Gbps
- Input common-mode range: extends 200 mV beyond rails
- LVDS output with 350 mV typical differential swing
- Supply voltage: 2.4 V to 5.5 V
- Mounted as IC1【9†tlv3604.pdf】

### LMH7220
- Propagation delay: 2.9 ns
- Input voltage range extends 200 mV below ground
- LVDS output designed for 100 Ω differential load
- Supply voltage: 2.7 V to 12 V
- Mounted as IC2【8†lmh7220.pdf】

## Connectors

### Power Supply (J1)

- Onboard filtering capacitors: 10 µF, 1 µF, and 100 nF
- 5.6 V Zener diode for optional input voltage clamping and reverse voltage protection

The module uses (2.4 V to 5.5 V) for the two comparators. Ensure proper voltages are applied as per the comparator requirements.

### Inputs

- **J2, J3**: Inputs for TLV3604 (IN+, IN-)
- **J4, J5**: Inputs for LMH7220 (IN+, IN-)

All inputs are via MCX connectors with ground-referenced shielding.

### Outputs

- **J6**: LVDS differential output from TLV3604 (TLV_OUT+, TLV_OUT-)
- **J7**: LVDS differential output from LMH7220 (LMH_OUT+, LMH_OUT-)

> Each output is routed to a standard 3-pin header: OUT+, GND, OUT-

## Notes

DNF (Do Not Fit) resistors R1 and R2 are placeholders for optional output termination.


