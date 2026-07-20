# Create Appointment with Quilia

## Endpoint

- **Method:** `POST`
- **Path:** `appointments`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Create Appointment](https://api.quilia.dev/v2#tag/appointments/POST/appointments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseId` | body | `string` | yes | The case ID to associate with the appointment. Links the appointment to a specific legal case or matter. |
| `contactId` | body | `string` | no | The contact/people ID associated with the appointment. Identifies the person involved in the appointment. Optional for legal appointments. |
| `notes` | body | `string` | no | Additional notes or details about the appointment. Can include agenda items, special instructions, or other relevant information. |
| `title` | body | `string` | no | Title/name of the appointment. Recommended for legal appointments. |
| `userId` | body | `string` | no | The user ID to assign the appointment to. If provided, this user will be responsible for the appointment. |
| `start` | body | `date` | yes | ISO 8601 timestamp for when the appointment starts. Must be a valid datetime string. |
| `end` | body | `date` | no | ISO 8601 timestamp for when the appointment ends. Required for legal appointments. |
| `type` | body | `list<string>` | no | Type of appointment: 'medical' for medical appointments, 'legal' for legal calendar events. Accepted values: `legal`, `medical`. |
