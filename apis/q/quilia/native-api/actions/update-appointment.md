# Update Appointment with Quilia

## Endpoint

- **Method:** `PATCH`
- **Path:** `appointments/:id`
- **Base URL:** `https://api.quilia.dev/v2`
- **Official documentation:** [Update Appointment](https://api.quilia.dev/v2#tag/appointments/PATCH/appointments/%7Bid%7D)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caseId` | body | `string` | no | The case ID to associate with the appointment |
| `contactId` | body | `string` | no | The contact/people ID to associate with the appointment |
| `id` | path | `string` | yes | The unique identifier of the appointment to update |
| `notes` | body | `string` | no | Additional notes or details about the appointment |
| `userId` | body | `string` | no | The user ID to assign the appointment to |
| `start` | body | `date` | no | ISO timestamp for the appointment start time |
| `end` | body | `date` | no | ISO timestamp for the appointment end time |
| `status` | body | `list<string>` | no | The status of the appointment Accepted values: `cancelled`, `confirmed`, `released`, `rescheduled`, `scheduled`. |
