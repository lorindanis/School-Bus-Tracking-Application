# School Bus Tracking & Safety System

This project is a real-time school bus tracking and student safety application backend prototype. It is designed to give parents and students peace of mind during daily commutes by integrating simulated onboard GPS telematics with student scanning hardware.

## Key Features

*   **Real-Time Fleet Telematics:** Simulates streaming live GPS coordinates from onboard bus tracking devices.
*   **Active Commute Window:** Parents and students can monitor live bus locations and receive dynamic ETAs (calculated via Haversine distance formula) only when the student is assigned to or currently on a route.
*   **Dual-Point Scan Verification:** Simulates students scanning an ID badge upon boarding and exiting the bus.
*   **Instant Parent Notifications:** Automated 'ping' alerts are sent to parent devices the moment a student scans on or off the vehicle, establishing a secure chain of custody.

## Getting Started

### Prerequisites
*   Python 3.x

### Running the Simulation
Execute the python script to run a mock morning commute:

```bash
python school_bus_tracker.py
```

## Architecture

The backend relies on Object-Oriented models:
*   `Student` & `Parent`: Data structures handling user relationships.
*   `Bus`: Manages routing, current coordinates, passenger manifestation, and ETA calculations.
*   `CommuteSystem`: Central orchestrator for scans, verifications, and status retrieval.
*   `NotificationSystem`: Handles outbound alerts to parents.
