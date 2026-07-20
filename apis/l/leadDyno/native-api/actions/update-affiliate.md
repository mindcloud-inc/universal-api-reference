# Update Affiliate with LeadDyno

Updates an existing affiliate in LeadDyno.

## Endpoint

- **Method:** `PUT`
- **Path:** `/affiliates/:id`
- **Base URL:** `https://api.leaddyno.com/v1`
- **Official documentation:** [Update Affiliate](https://app.theneo.io/leaddyno/leaddyno-rest-api/affiliates/put-affiliates-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The email address of the affiliate. |
| `first_name` | body | `string` | no | The first name of the affiliate. |
| `id` | path | `number` | yes | The affiliate ID. |
| `last_name` | body | `string` | no | The last name of the affiliate. |
