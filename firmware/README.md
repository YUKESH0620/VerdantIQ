# Development Roadmap

This roadmap is ordered by dependency and evidence. No completion is implied by the presence of a phase. Mark a phase complete only when its criterion is supported by a recorded result.

| Phase | Goal | Measurable completion criterion |
|---:|---|---|
| 1 | Define the project architecture and preliminary BOM. | Architecture document, interface assumptions, safety boundaries, and editable BOM reviewed; unresolved decisions listed. |
| 2 | Set up the Nordic development kit and verify the toolchain. | A documented build/flash/debug or equivalent bring-up procedure succeeds on the selected environment, with board and SDK versions recorded. |
| 3 | Implement sensor acquisition and measurement validation. | At least one selected sensor produces timestamped readings, and invalid/out-of-range behavior is demonstrated with recorded observations. |
| 4 | Establish Bluetooth communication with a compatible sensor node. | A node exchanges identified, timestamped test data with the Nordic controller across the intended test setup, including lost-link handling. |
| 5 | Implement equipment-health monitoring using thresholds and trends. | Recorded motor, pump, temperature, flow, battery, or related signals trigger documented test anomalies and produce repeatable classifications or events. |
| 6 | Deliver farmer alerts and actionable recommendations. | A representative abnormal condition reaches the farmer interface with an understandable alert, recommended next step, and defined acknowledgement or escalation behavior. |
| 7 | Integrate Nordic, ESP32, and the farmer's base unit. | A versioned interface exchanges health/status and command messages, handles timeout/reset cases, and leaves actuators in defined safe states. |
| 8 | Run smart-irrigation and resource-monitoring experiments. | A controlled test compares commanded irrigation with measured flow and soil response, with water-use data and limitations recorded. |
| 9 | Develop crop imaging, disease-detection integration, pesticide application, and night-patrol functions. | Each function has a defined test setup, safety boundary, representative data or scenarios, and documented performance/limitations; no capability is accepted solely by demonstration video. |
| 10 | Perform integrated system testing, field validation, and sustainability measurements. | Test results include reliability, false alerts, resource-use observations, safety outcomes, and clearly stated environmental/test conditions. |
| 11 | Evaluate future Raspberry Pi migration. | A comparison based on measured processing, storage, latency, power, and integration needs supports a documented keep-or-migrate decision. |

## Relationship to current progress

The farmer's base-unit firmware has already been written, and its hardware setup and integration are underway. The roadmap therefore begins with architecture and validation while preserving the base unit as an active integration stream; it does not imply that the base unit is unstarted or fully complete.

## Evidence policy

For each phase, retain the relevant configuration, test notes, logs, measurements, and limitations. A successful build is not the same as a validated field capability, and a threshold alarm is not by itself predictive maintenance. Historical operating data and outcome validation are required before making failure-prediction claims.
