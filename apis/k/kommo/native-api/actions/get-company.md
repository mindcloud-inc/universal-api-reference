# Get Company with Kommo

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Get Company](https://developers.kommo.com/reference/get-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Company ID. |
| `with` | query | `string` | no | Comma-separated related resources to include. |
