# Salix-AOM-control

This repository contains code for a Labview application for controlling the power of the 515 nm and 561 nm in the C-Flex laser combiner on _Salix_. These two lasers are Diode-Pumped Solid State (DPPS) lasers and should be run at maximum power for optimal performance. There are two acouso-optic modulators (AOM) inside the C-Flex enclosure in the optical path of these two lasers (one for each laser). By placing a different voltage over the AOMs, the transmission through the AOM can be modulated between (nearly) 0% up to 100%.

The Labview application lets the user set a _transmission percentage_ (labeled _Power (%)_ in the gui) for each laser using a slider. This percentage is converted to a voltage value (0-100% is linearly scaled to 0.5V-1.0V). These voltage values are written to the AO0 and AO1 channels (AO0 for 515 nm and AO1 for 561 nm) of a multi-function DAQ device (USB-6002, National Instruments) via USB. A lead from each channel (and AO ground) is terminated in a male BNC connector, to connect to the respective AOM controller.

# Hardware setup

The multi-function DAQ device (USB-6002, National Instruments)
