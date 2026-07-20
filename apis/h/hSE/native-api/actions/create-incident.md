# Create Incident with 4HSE

Creates a new incident in 4HSE.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/incident/create`
- **Base URL:** `https://service.4hse.com`
- **Official documentation:** [Create Incident](https://docs.4hse.com/en/api/incident/#operation-createIncident-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | no | Identifier code. |
| `name` | body | `string` | yes | Title or name of the incident. |
| `date_incident` | body | `date` | yes | Date when the incident occurred. |
| `category` | body | `string` | no | Incident category. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `description_event` | body | `string` | no | Description of what happened. |
| `status` | body | `string` | no | Workflow status. Accepted values: `0`, `1`, `2`. |
| `subtenant_id` | body | `string` | yes | The office where the incident occurred. |
| `tenant_id` | body | `string` | yes | The project the incident belongs to. |
