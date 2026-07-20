# Update Lead with LeadDyno

Updates an existing lead in LeadDyno.

## Endpoint

- **Method:** `PUT`
- **Path:** `/leads/:id`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Update Lead](https://app.theneo.io/leaddyno/leaddyno-rest-api/leads/update-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | The first name of the lead. |
| `id` | path | `number` | yes | The lead ID. |
| `last_name` | body | `string` | no | The last name of the lead. |
| `email` | body | `string` | yes | The email address of the lead. |
