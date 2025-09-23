**New Filter Options for Enhanced Statistical Analysis**

I've recently added two new filter options to enhance statistical analysis in our simulations.  The `DemuxAppFilter` simplifies partitioning results based on the packet's source application, making it easier to isolate and analyze data from specific sources.  Complementing this, the `DemuxRegexFilter` offers more advanced partitioning by allowing users to define regular expressions based on the name of the details object. This enables fine-grained control over data partitioning, allowing for more complex analyses.  For instance, you could use this filter to partition `packetLifeTime` based on the packet name, effectively tracing the lifespan of packets originating from different applications. -Levente Meszaros

**Improved Packet Lifetime Statistics**

To make our simulations more user-friendly, I've added a new `packetLifeTime` statistic wherever `meanBitLifeTimePerPacket` is present. I found that `meanBitLifeTimePerPacket` can be a bit confusing in its name and description. `packetLifeTime` provides a more straightforward and intuitive measure of packet lifetime, improving clarity and interpretation. -Levente Meszaros

**Introducing the PacketLifeTimeFilter**

I've implemented a new result filter called `PacketLifeTimeFilter`. This filter calculates the scalar lifetime for the entire data portion of a packet, when applicable.  This provides a concise summary of how long the packet data spends in the system, useful for performance analysis. -Levente Meszaros

**Visualizing Chart Test Differences with a Python GUI**

I've developed a Python GUI application that visually presents the differences identified by our chart tests. This tool will significantly streamline our testing and debugging workflow, allowing us to quickly pinpoint and address discrepancies in our chart outputs. -Levente Meszaros

**Addressing BGP Session Timeout Errors**

I fixed a bug where the `sessionEstablished` flag in the BGP finite state machine (FSM) was not being reset when transitioning to the Idle state. This issue led to errors in simulations with multiple BGP routers, where sessions would timeout before completing information exchange.  The problem has been resolved by ensuring that `sessionEstablished` is reset to false whenever the FSM enters the Idle state.  This fix improves the stability of BGP simulations, particularly in larger network scenarios.  -Zoltan Bojthe

**Enhanced Ethernet Support: 800 Gbps Added**

I've expanded our Ethernet support to include the 800 Gbps rate.  This addition reflects the ongoing advancements in network technology and enables simulations of cutting-edge high-speed networks. -Zoltan Bojthe


**Improving Fingerprint Difference Analysis**

I've implemented some fixes and enhancements to the `inet_diffingerprints` tool. The tool now correctly displays differences even when the unique fingerprint lists have varying lengths.  I've also redesigned the `readFingerprints()` function to return a more structured list of [event number, fingerprint] pairs, improving the tool's overall functionality and usability. -Zoltan Bojthe


