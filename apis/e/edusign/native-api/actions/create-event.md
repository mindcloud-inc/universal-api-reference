# Create Event with Edusign

Creates a new event in Edusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Create Event](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apiIdMode` | query | `string` | no | Switch between internal IDs and external API IDs for students/professors <br><strong style="color:gold">Important:</strong> When enabled, use external API IDs in the students and professors arrays instead of internal Edusign IDs. |
| `name` | body | `string` | yes | Event title (required) |
| `description` | body | `string` | no | Detailed description of the event (optional) |
| `start` | body | `string` | yes | Event start date and time (required, format: ISO 8601, e.g., "2020-01-20T15:00:00.000Z") |
| `end` | body | `string` | yes | Event end date and time (required, format: ISO 8601, e.g., "2020-01-20T18:00:00.000Z") |
| `professors[]` | body | `array<string>` | no | — |
| `students[]` | body | `array<string>` | no | — |
| `classroom` | body | `string` | no | Classroom or location name (will be automatically created if it doesn't exist) |
| `apiId` | body | `string` | yes | External API identifier for this event (required for tracking and updates) |
| `apiType` | body | `string` | no | Source system or category for the external API (e.g., "calendar_system") |
| `color` | body | `string` | no | Display color for the event in hex format (e.g., "#4c00ff") |
