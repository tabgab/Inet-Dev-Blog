## Development Blog Entries


**New Feature: Clock Granularity Control in Oscillator-Based Clocks**

I've added a new parameter, `clockGranularity`, to the `OscillatorBasedClock` class. This parameter allows for finer control over the clock's precision, enabling simulations to more accurately model real-world timing behavior.  This enhancement provides greater flexibility in simulating systems with specific timing requirements. - *Levente Meszaros*


**Improved Clock Parameter Naming for Clarity**

In an effort to improve code readability and maintainability, I've renamed a parameter in the `SettableClock` class from a less descriptive name to `initialOscillatorCompensation`. This change makes the purpose of the parameter clearer and contributes to a more understandable codebase. - *Levente Meszaros*


**Enhanced Simulation Timing with Oscillator Compensation**

I've implemented frequency compensation in the clock mechanism.  This addresses potential inaccuracies in simulated time by adjusting the clock based on oscillator behavior.  This improvement leads to more reliable and realistic simulation results, especially in scenarios with varying oscillator frequencies. - *Levente Meszaros*



**Strengthened Clock Event Ordering Assertions**

I've enhanced the robustness of the clock implementation by adding assertions to ensure the correct ordering of clock events. This helps in early detection of potential issues related to event scheduling, improving the reliability and predictability of simulation runs. Additionally, I've moved some definitions to `DebugDefs.h` for better organization.  - *Levente Meszaros*
