# Get Lead with Kommo

## Endpoint

- **Method:** `GET`
- **Path:** `/leads/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Get Lead](https://developers.kommo.com/reference/getting-a-lead-by-its-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Lead ID. |
| `with` | query | `string` | no | Comma-separated related resources to include. |
