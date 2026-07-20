# Update Appointment with Follow Up Boss

Updates an existing appointment in Follow Up Boss.

## Endpoint

- **Method:** `PUT`
- **Path:** `appointments/:id`
- **Base URL:** `https://api.followupboss.com/v1/`
- **Official documentation:** [Update Appointment](https://docs.followupboss.com/reference/appointments-id-put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The appointment ID. |
| `invitees[].personId` | body | `number` | no | — |
| `invitees[].userId` | body | `number` | no | — |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `start` | body | `date` | no | — |
| `end` | body | `date` | no | — |
| `timezone` | body | `string` | no | — |
| `location` | body | `string` | no | — |
