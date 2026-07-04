# TCP-Signal Visualization App
## Project goal
The goal of this project is to develop a PySide6 desktop application for live visualization and offline inspection of multi‑channel signal data streamed via TCP from a dedicated server. The software will act as a client that connects to the existing TCP server, receives continuous data packets, and makes them accessible for analysis in an intuitive graphical user interface.

Specifically, the application aims to:
- Provide a reliable TCP connection interface, including port configuration, connection status feedback, and start/stop streaming controls.
- Implement robust data handling for 32 channels × 18 samples per packet, converting raw byte streams into numerical arrays suitable for processing.
- Offer real-time visualization of selected channels using VisPy, with a rolling time window, readable axes, and a clear way to switch between channels.
- Enable a Plot All Channels view to quickly inspect simultaneous activity across all 32 channels, using vertical offsets to keep the signals readable.
- Support multiple signal modes (original, RMS, and filtered) for both live and offline views, allowing users to compare different processing approaches.
- Provide offline inspection of recorded signals with Matplotlib, including channel selection and mode switching after streaming has stopped.
- Follow an MVVM-style architecture to separate concerns between data models, viewmodels (application logic and state), and views (GUI and plotting).
- Include basic error handling for common issues such as unavailable server, wrong port, lost connection, or invalid user selections, without crashing the application.
- Deliver clear documentation and dependency management so that the application can be installed and run on a clean environment using only the listed packages.