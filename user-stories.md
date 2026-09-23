# User Stories

## User Story 1: Reschedule Appointment

As a patient, I want to reschedule my appointment so that I can choose a more convenient date and time.

### Acceptance Criteria

#### Scenario: Patient reschedules an appointment within 24 hours of window

**Given** a patient has a scheduled appointment for `2026-10-15T10:00:00Z`

**When** the patient requests a reschedule to `2026-10-16T14:00:00Z` less than 24 hours before the original time

**Then** the system should apply a late-change flag

**And** emit an `AppointmentRescheduled` event to the Notification Service

**And** display a confirmation message with updated details to the patient
