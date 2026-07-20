# Create a New Appointment with Mihu AI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/appointments`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Create a New Appointment](https://developers.mihu.ai/api-reference/appointments/create-a-new-appointment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_uuid` | body | `string` | no |
| `description` | body | `string` | no |
| `end_time` | body | `string` | yes |
| `notes` | body | `string` | no |
| `schedule_uuid` | body | `string` | yes |
| `start_time` | body | `string` | yes |
| `status` | body | `string` | no |
| `title` | body | `string` | yes |
