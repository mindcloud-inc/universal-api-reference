# Get Book by ISBN with Brasil API

Retrieves book details from Brasil API by ISBN.

## Endpoint

- **Method:** `GET`
- **Path:** `/isbn/v1/{isbn}`
- **Base URL:** `https://brasilapi.com.br/api`
- **Official documentation:** [Get Book by ISBN](https://brasilapi.com.br/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isbn` | path | `string` | yes | The ISBN code to look up. |
| `providers` | query | `string` | no | Optional comma-separated ISBN providers. |
