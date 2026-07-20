# Update Appointment with Freshworks CRM

Updates an existing appointment in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/appointments/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Appointment](https://developers.freshworks.com/crm/api/#update_an_appointment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `appointment` | body | `object` | yes |
| `appointment.description` | body | `string` | no |
| `appointment.end_date` | body | `string` | no |
| `appointment.from_date` | body | `string` | no |
| `appointment.location` | body | `string` | no |
| `appointment.targetable_id` | body | `number` | no |
| `appointment.targetable_type` | body | `string` | no |
| `appointment.time_zone` | body | `string` | no |
| `appointment.title` | body | `string` | no |
| `id` | path | `string` | yes |
