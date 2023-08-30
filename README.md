# Micro machine simulation in TwinCAT and TwinCAT HMI

This repository serves as an introduction to simple PLC programming concepts, the following basic ideas are shown:

### PLC
- State machine
    - Improved readability through use of enums
    - Control through external booleans (optionally from an included HMI project)
- Timer
- Heartbeat variable to signal machine health
- Random numbers

### HMI
- Direct button bindings
- Showing text in textblocks
- Using textblocks as labels

In addition, some more advanced concepts are shown:

### PLC
- Separate functions for the MAIN program

### HMI
- Reading enumerations as strings through some intermediate javascript.
- Dynamically changing the color of elements

When reading an enumeration directly as a data binding only the integer representation is passed through the binding. However, with knowledge of the datatype we can easily recover the desired `<integer> => <string>` binding.
The `TcHmi` namespace provides an `EnumToString` function, but that requires a list of enumeration values. So this function will not react automatically to PLC enum definition changes. There are ways around this, but encapsulating it in a single function as shown in this example is less error prone.

## Instructions
1. Simply open the TwinCAT XAE shell or Visual Studio and choose `File->Open->Open Solution from Archive...`.
2. Check if the PLC compiles and activate the configuration
3. Either
    1. Open the HMI live view to control the machine simulation or,
    2. Trigger the booleans in the PLC live view.
4. Have fun!

### Versions
- Made with 
    - TwinCAT 3.1.4024.47
    - TwinCAT HMI TE2000 1.12.760.44


#### Disclaimer
This project is not intended to show correct programming practices, it is solely meant as an easy, readable, and mostly fun introduction to some concepts.