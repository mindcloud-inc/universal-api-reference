# Create Appointment with Freshworks CRM

Creates a new appointment in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/appointments`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Appointment](https://developers.freshworks.com/crm/api/#create_appointment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `appointment` | body | `object` | yes |
| `appointment.description` | body | `string` | no |
| `appointment.end_date` | body | `string` | yes |
| `appointment.from_date` | body | `string` | yes |
| `appointment.location` | body | `string` | no |
| `appointment.targetable_id` | body | `number` | yes |
| `appointment.targetable_type` | body | `string` | yes |
| `appointment.time_zone` | body | `string` | no |
| `appointment.title` | body | `string` | yes |
