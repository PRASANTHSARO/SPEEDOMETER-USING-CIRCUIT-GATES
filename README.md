
# Automobile Speed Sensor Decoder and 7-Segment Display

## Overview
This project involves designing a decoder circuit that processes a 4-bit encoded speed sensor reading in an automobile and triggers appropriate speed indicators—Slow, Economy, and Fast. The project also includes a circuit to display the speed category ("S", "E", or "F") on a 7-segment display. The design utilizes basic digital logic components including AND, OR, XOR, and NOT gates.

## Components Used
- **Quad AND Gate (IC7408)**: Contains four 2-input AND gates for logical conjunction.
- **Quad OR Gate (IC7432)**: Contains four 2-input OR gates for logical disjunction.
- **Quad XOR Gate (IC7486)**: Contains four 2-input XOR gates for exclusive OR operations.
- **NOT Gate (IC7404)**: Provides inversion of input signals.
- **Triple 3-input AND Gate (IC7411)**: Provides three independent 3-input AND gates.
- **7-Segment Display**: Displays the letters "S", "E", or "F" based on the decoded speed category.
- **Resistors (1 k-ohm)**: Used for current regulation in the circuit.
- **Breadboard**: For assembling the circuit.
- **Digital IC Trainer**: For powering and testing the circuit.
- **Connecting Wires**: For making the necessary connections between components.

## Design Details

### Triggering S, E, F:
The speed sensor provides a 4-bit encoded output (S3 S2 S1 S0). The decoder determines the speed category based on the following logic:
- **Slow (S)**: Asserted when the sensor output is between 0 and 5.
- **Economy (E)**: Asserted when the sensor output is between 6 and 12.
- **Fast (F)**: Asserted when the sensor output is between 13 and 15.

### 7-Segment Display:
The circuit controls the 7-segment display to show "S" for Slow, "E" for Economy, and "F" for Fast. The corresponding segments are activated based on the decoded speed category.

## Truth Tables

### Triggering Logic:
| S3 | S2 | S1 | S0 | S | E | F |
|----|----|----|----|---|---|---|
|  0 |  0 |  0 |  0 | 1 | 0 | 0 |
|  0 |  0 |  0 |  1 | 1 | 0 | 0 |
|  0 |  0 |  1 |  0 | 1 | 0 | 0 |
|  0 |  0 |  1 |  1 | 1 | 0 | 0 |
|  0 |  1 |  0 |  0 | 1 | 0 | 0 |
|  0 |  1 |  0 |  1 | 1 | 0 | 0 |
|  0 |  1 |  1 |  0 | 0 | 1 | 0 |
|  0 |  1 |  1 |  1 | 0 | 1 | 0 |
|  1 |  0 |  0 |  0 | 0 | 1 | 0 |
|  1 |  0 |  0 |  1 | 0 | 1 | 0 |
|  1 |  0 |  1 |  0 | 0 | 1 | 0 |
|  1 |  0 |  1 |  1 | 0 | 1 | 0 |
|  1 |  1 |  0 |  0 | 0 | 1 | 0 |
|  1 |  1 |  0 |  1 | 0 | 0 | 1 |
|  1 |  1 |  1 |  0 | 0 | 0 | 1 |
|  1 |  1 |  1 |  1 | 0 | 0 | 1 |

### 7-Segment Display Logic:
| S | E | F | a | b | c | d | e | f | g |
|---|---|---|---|---|---|---|---|---|---|
| 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 | 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 1 | 0 | 1 | 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 1 | 0 | 1 | 1 | 0 | 1 | 1 |
| 1 | 0 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 0 |

## Acknowledgments
1. **Digital Logic Design**: Fundamental concepts used to design the decoder and 7-segment display logic.
2. **7-Segment Display**: Standard display unit used in many digital electronics applications.
