# Update Deal with Teamgate

Updates a deal in Teamgate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/deals/:deal_id`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Update Deal](https://developers.teamgate.com/#fe590427-fcb9-4689-9671-7d3daa235b1a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal_id` | path | `string` | yes | Deal ID to update. |
| `name` | body | `string` | no | Updated deal name. |
