# Context Diagram

## Patient Appointment System

```mermaid
flowchart TD
    Patient[Patient]
    System[Patient Appointment System]
    Notification[Notification Service]

    Patient -->|Schedule, reschedule or cancel appointment| System
    System -->|Appointment confirmation and updated details| Patient
    System -->|Appointment notification event| Notification
    Notification -->|Notification status| System
