# Update Appointment Status with Mihu AI

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/appointments/:uuid/status`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Update Appointment Status](https://developers.mihu.ai/api-reference/appointments/update-appointment-status)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `status` | body | `string` | yes |
| `uuid` | path | `string` | yes |
