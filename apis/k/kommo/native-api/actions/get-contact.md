# Get Contact with Kommo

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Get Contact](https://developers.kommo.com/reference/get-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact ID. |
| `with` | query | `string` | no | Comma-separated related resources to include. |
