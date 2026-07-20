# Create Appointment with Follow Up Boss

Creates a new appointment in Follow Up Boss.

## Endpoint

- **Method:** `POST`
- **Path:** `appointments`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [Create Appointment](https://docs.followupboss.com/reference/appointments-post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `invitees[].personId` | body | `number` | no |
| `invitees[].userId` | body | `number` | no |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
| `start` | body | `date` | no |
| `end` | body | `date` | no |
| `timezone` | body | `string` | no |
| `location` | body | `string` | no |
