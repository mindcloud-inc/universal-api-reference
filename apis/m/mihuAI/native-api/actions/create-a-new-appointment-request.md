# Create a New Appointment Request with Mihu AI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/appointment-requests`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Create a New Appointment Request](https://developers.mihu.ai/api-reference/appointment-requests/create-a-new-appointment-request)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_email` | body | `string` | no |
| `contact_name` | body | `string` | no |
| `contact_phone` | body | `string` | no |
| `contact_surname` | body | `string` | no |
| `contact_uuid` | body | `string` | no |
| `description` | body | `string` | no |
| `end_time` | body | `string` | no |
| `notes` | body | `string` | no |
| `schedule_uuid` | body | `string` | yes |
| `start_time` | body | `string` | yes |
| `title` | body | `string` | yes |
