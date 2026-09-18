# -Mars-Rover-Mission-Control-
Requirements analysis for the mars rover mission control system, including functional and non-functional, and updated CR requirements.
### Functional Requirements (FRs)
* **FR-01 (Movement Execution):** The rover shall receive movement commands from Mission Control and execute valid commands.
* **FR-02 (Telemetry Reporting):** The rover shall report its current position, battery level, temperature, and communication status.
* **FR-03 (Command Validation):** The system shall reject invalid or unauthorized commands.
* **FR-04 (Emergency Safety - Original):** The rover shall enter Safe Mode when a critical battery or thermal condition is detected.
* **FR-05 (Execution Feedback):** Mission Control shall receive command execution status.
* **FR-06 (Event Logging):** All commands and critical rover events shall be recorded with timestamp and operator ID.
* ### Non-Functional Requirements (NFRs)
* **NFR-01 (Performance):** Command processing should normally complete within 5 seconds after a command is received by the rover.
* **NFR-02 (Security - Original):** Only authenticated Mission Control operators shall be permitted to issue rover commands.
* **NFR-03 (Reliability):** The system shall continue operating despite temporary communication interruptions.
* **NFR-04 (Scalability - Original):** The system should support communication with multiple rovers simultaneously.
## 2. Mission Control Change Requests (CRs)

### Change Request CR-01: Emergency Safety Thresholds
* **Target Requirement:** FR-04
* **Original:** The rover shall enter Safe Mode when a critical battery or thermal condition is detected.
* **Updated Requirement:** The rover shall enter Safe Mode within 3 seconds when battery temperature exceeds the critical threshold or battery capacity falls below the defined emergency level.
* ### Change Request CR-02: Mission Expansion
* **Target Requirement:** NFR-04.
* **Original:** The system shall support communication with multiple rovers simultaneously.
* **Updated Requirement:** The system shall support at least 20 simultaneously connected rovers.
* ### Change Request CR-03: Security Upgrade
* **Target Requirement:** NFR-02.
* **Original:** Only authenticated Mission Control operators shall be permitted to issue rover commands.
* **Updated Requirement:** The system shall require authenticated and role-authorized operators before accepting rover commands.
