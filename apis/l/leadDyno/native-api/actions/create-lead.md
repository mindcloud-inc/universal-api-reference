# Create Lead with LeadDyno

Creates a new lead in LeadDyno.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Create Lead](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/create-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address of the lead. |
| `tracking_code` | body | `string` | no | The tracking code assigned to the lead. |
