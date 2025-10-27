# 🔥 LoRa Wildfire Alert Network

### Senior Computer Science Capstone Project — Class of 2026

Oregon’s wildfire season, spanning from mid-May through late September, has become increasingly destructive due to climate change, drier conditions, and decades of fuel accumulation. These factors have led to larger, more intense, and harder-to-contain fires that threaten lives, destroy timberlands and watersheds, and devastate habitats critical to Oregon communities (wfca_teila, 2023). The urgency of this problem was underscored on August 21, 2025, when a wildfire near Sisters, Oregon expanded to 18,000 acres in just two days with 0% containment, forcing widespread evacuations and demanding massive firefighting resources (Isaksen, 2025).

Current wildfire detection efforts in Oregon rely heavily on AI-enabled camera networks operated by the Oregon Hazards Lab (OHAZ), which can identify smoke plumes up to 40 miles away. While technologically advanced, this approach is inherently reactive, as detection begins only after smoke is visible—often when fires are already spreading (OHAZ, 2025).

The motivation behind the ECE project is to develop a proactive, ground-level monitoring system that can detect environmental precursors to wildfire—such as sudden temperature spikes, sharp drops in humidity, or elevated smoke particulates—before smoke plumes appear. By designing low-power, solar-enabled LoRa sensor nodes, the team aims to provide earlier alerts that complement the existing camera network, giving firefighters and communities valuable time to respond before small ignitions escalate into uncontrollable wildfires.

Our goals are:

Gateway Development
- Implement software to receive LoRa packets and forward them to a lightweight backend using necessary communication protocols.
- Add lightweight reliability features (acknowledgments, retries, sequence numbers) at the application level to ensure dependable delivery.

Backend & Dashboard
- Build a lightweight backend that logs sensor readings into persistent storage for analysis.
- Develop a responsive web dashboard to visualize:
  - Sensor health and environmental data.
  - Battery status of each node.
  - Alert conditions and thresholds.
  - Deployment maps with fixed node coordinates, using Leaflet.js or a comparable mapping framework.
  - A list view of nodes sortable by recent communication, battery level, or triggered thresholds.
  - Heatmaps to visualize patterns and scale of environmental changes.
- Implement a button-operated automated alert system that issues SMS/email notifications to emergency personnel.
- Provide export functions such as screenshots, printouts, or coordinate lists for authorities and maintenance crews.

System Enhancements
- Support anomaly detection and trend visualization (e.g., temperature/humidity over time) using stored data.
- Spool simulated sensor data to validate system performance.
- Add end-to-end security: AES encryption for LoRa packets.

---

## Project Overview

| Component | Description |
|------------|-------------|
| **LoRaWAN Sensor Nodes** | ESP32-based environmental monitoring units with LoRa transceivers |
| **LoRa Gateway** | Receives sensor packets and forwards them via MQTT |
| **Cloud Webhook & Backend** | API for ingesting, storing, and visualizing alert data |
| **Visualization Dashboard** | Web UI to monitor live sensor readings and alert events |

---

## Tech Stack

- **Hardware:** ESP32, LoRa 
- **Protocols:** LoRaWAN, MQTT, HTTP/S  
- **Backend:** Chirpstack 
- **Frontend:** TBD
- **Data Storage:** PostgreSQL
- **Deployment:** Docker

---

## Key Repositories

- [**LoRaWAN-Wildfire**](https://github.com/LoRa-Wildfire-Alert-Network/LoRaWAN-Wildfire) — Chirpstack server, device and gateway configuration
- [**lorawan-node-simulator**](https://github.com/LoRa-Wildfire-Alert-Network/Dashboard) — Web Dashboard and database to visualize node data and device metrics

---

## Team Members

| Name | Role | Focus |
|------|------|--------|
| Derek Greene | Systems Engineer | Gateway + Backend Integration |
| Derek Knowlton | Web Developer | Web Dashboard + Database |
| Zac Speiser | Hardware/Software Developer | Microprocessor Design + Database |
| Gaurav Dange | Hardware Developer | ... |
| Juan Chan Vasquez | Hardware Developer | ... |
| Andrew Liang | Hardware Developer | ... |
| Andrew Liang | Hardware Developer | ... |

---

## License

This project is open-source under the **MIT License**.  

---

### “Saving forests, one packet at a time”
