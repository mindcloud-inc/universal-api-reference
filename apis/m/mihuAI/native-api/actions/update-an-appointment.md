# Update an Appointment with Mihu AI

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/appointments/:uuid`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Update an Appointment](https://developers.mihu.ai/api-reference/appointments/update-an-appointment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `end_time` | body | `string` | no |
| `start_time` | body | `string` | no |
| `status` | body | `string` | no |
| `title` | body | `string` | no |
| `uuid` | path | `string` | yes |
