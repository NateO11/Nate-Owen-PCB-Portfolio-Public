# Interactive Toy Project Overview

This project involved the design and development of an embedded interactive toy centered around a custom printed circuit board integrating sensing, actuation, wireless communication and battery powered operation. The system was created to enable responsive user interaction through motion, lighting, sound and wireless connectivity. The project was developed as an assistive toy designed to provide engaging sensory feedback and accessible interaction for a child with cerebral palsy.

The hardware supports multiple interactive subsystems driven by an ESP32 microcontroller, including:

- LED control

- Vibration motors

- Audio output

- Force sensing input

- Bluetooth Low Energy communication

- Battery powered operation

A primary engineering challenge was designing a reliable power architecture capable of supporting highly dynamic loads, specefically LED and motor current spikes, while maintaining stable 3.3 V logic rails required for wireless communication and sensor accuracy.

Key power design considerations included:

- Voltage regulator selection

- Separation of power and logic rails

- Decoupling capacitance placement

- Brownout prevention during peak load 

A major focus of the project was PCB organization and system modularity. High current paths were intentionally separated from sensitive communication circuitry to reduce electrical noise and simplify debugging.

Communication interfaces were selected based on subsystem requirements:

- SPI for timing peripherals

- I2C to reduce pin usage and allow for scaleabilty

Layout decisions prioritized electrical performance and manufacturability:

- Short current return paths

- Controlled grounding

- Noise isolation between subsystems

- Connector placement aligned with enclosure constraints

Because the device operates as a battery powered consumer system, electrical reliability and thermal behavior were critical design constraints.

Engineering Challenges

One of the most significant challenges occurred during early PCB iterations when programming access to the microcontroller was unintentionally omitted. This prevented firmware flashing and required a full board redesign.

This experience directly influenced improvements to the development workflow:

1. Structured schematic review before fabrication

2. Firmware and hardware pin mapping

3. Inclusion of dedicated interfaces

4. Incremental subsystem validation prior to integration
