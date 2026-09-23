# Acceptance Criteria

## Scenario: Patient reschedules an appointment within 24 hours of window

### Given
A patient has a scheduled appointment for `2026-10-15T10:00:00Z`.

### When
The patient requests a reschedule to `2026-10-16T14:00:00Z` less than 24 hours before the original time.

### Then
The system should apply a late-change flag.

### And
The system should emit an `AppointmentRescheduled` event to the Notification Service.

### And
The system should display a confirmation message with the updated appointment details to the patient.
