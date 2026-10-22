# Preliminary Bill of Materials

This is an **initial, editable engineering BOM** for VerdantIQ. It is a planning document, not evidence that every component has been selected, purchased, assembled, or tested. Revise it as the architecture, interfaces, safety requirements, and procurement plan are finalized.

Add exact part numbers, quantities, suppliers, prices, and procurement status when known. Use `TBD` where a decision remains open.

| Item | Component | Purpose | Quantity | Status | Specifications or notes |
|---:|---|---|---:|---|---|
| 1 | Nordic nRF54LM20 DK | Dedicated embedded control, validated sensor acquisition, Bluetooth-connected sensor networking, equipment-health monitoring, safety checks, and edge-AI evaluation | 1 | Requested for contest | Confirm supported peripherals, SDK/toolchain, memory, timing, and interface compatibility before implementation |
| 2 | ESP32 main-controller development board | Initial high-level rover brain, mission execution, and subsystem coordination | 1 | Planned | Exact board and interface allocation TBD |
| 3 | ESP32-CAM or suitable vision platform | Crop and field image capture and vision processing within actual platform capabilities | 1 | Under evaluation | Select according to camera needs, processing, storage, lighting, and model requirements |
| 4 | Soil-moisture sensors | Measure soil condition for irrigation decisions and field monitoring | TBD | Under evaluation | Sensor technology, placement, calibration, ingress protection, and quantity TBD |
| 5 | Environmental temperature and humidity sensors | Monitor field and equipment environmental conditions | TBD | Planned | Locations, accuracy, protection, and interface TBD |
| 6 | Motor-current sensing hardware | Detect load changes, stalls, blockage, and other motor or pump abnormalities | TBD | Under evaluation | Select shunt, current-sense IC, or other suitable method after power measurements are known |
| 7 | Motor or pump temperature sensor | Detect overheating and support equipment-health monitoring | TBD | Under evaluation | Sensor type and mounting method TBD |
| 8 | Water-flow sensor | Confirm irrigation flow and identify possible blockage, leakage, or dry-running behavior | TBD | Under evaluation | Flow range, pressure loss, fluid compatibility, and pulse/interface details TBD |
| 9 | Motor drivers | Safely control rover motors and any applicable DC loads | TBD | Planned | Current, voltage, protection, thermal limits, and control interface TBD |
| 10 | Irrigation pump and valve driver circuits | Switch and protect irrigation pumps and valves | TBD | Planned | Use appropriate external drivers, flyback/protection, isolation where needed, and safe default states |
| 11 | Bluetooth-compatible distributed sensor-node hardware | Collect and transmit soil/environment data from different farm locations | TBD | Under evaluation | Node MCU, sensors, power source, enclosure, protocol, and range require validation; no guaranteed range assumed |
| 12 | Rover chassis, motors, and wheels | Mobile mechanical platform | TBD | Planned | Payload, terrain, traction, speed, ingress protection, and motor sizing TBD |
| 13 | Battery and power-management components | Supply regulated power to logic, sensors, actuators, and communications | TBD | Under evaluation | Battery chemistry, capacity, protection, charging, rails, fusing, and power budget TBD |
| 14 | Controlled pesticide-delivery mechanism | Deliver approved treatment under defined rules and farmer oversight | TBD | Planned | Tank, pump, nozzle, metering, interlocks, calibration, containment, and safety requirements TBD |
| 15 | Night-patrol sensing hardware | Detect possible animal intrusion during patrols and raise alerts | TBD | Under evaluation | Camera, illumination, motion, thermal, or other sensing approach TBD; detection is not guaranteed |
| 16 | Additional base-unit hardware | Support the existing farmer handheld base unit where genuinely required | TBD | Existing — details to be confirmed | Do not infer exact components or protocol until the existing base-unit design is documented |
| 17 | Wiring, connectors, fuses, and protection | Reliable and serviceable interconnection and power protection | TBD | Planned | Select for current, environment, vibration, sealing, and serviceability |
| 18 | Enclosures and environmental protection | Protect electronics and sensors from dust, moisture, chemicals, and field conditions | TBD | Planned | IP rating, thermal behavior, access, and material compatibility TBD |
| 19 | Emergency stop/manual override hardware | Provide a defined safe way to stop or disable hazardous motion and fluid delivery | TBD | Planned | Placement, latching behavior, reset behavior, and actuator safe states TBD |
| 20 | Data logging and storage hardware | Record sensor and operating data for validation and future predictive-maintenance analysis | TBD | Under evaluation | Storage medium, retention, timestamping, and data export method TBD |

## BOM revision checklist

Before marking an item selected or procured, record:

- Exact manufacturer and part number.
- Quantity and installation location.
- Electrical, mechanical, environmental, and safety constraints.
- Interface and pin/resource requirements.
- Supplier, price, lead time, and procurement status.
- Validation status and any replacement options.

The Nordic board's intended role is to provide a dedicated, testable embedded-control and monitoring layer—not to replace the ESP32's high-level coordination or the vision platform's image-processing responsibilities.
