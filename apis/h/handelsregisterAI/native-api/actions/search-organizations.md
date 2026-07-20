# Search Organizations with Handelsregister AI

Finds organizations in Handelsregister AI by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search-organizations`
- **Base URL:** `https://handelsregister.ai/api/v1`
- **Official documentation:** [Search Organizations](https://handelsregister.ai/en/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Company name, registration number, or search query. |
| `limit` | query | `number` | no | Maximum number of results to return (default: 10, max: 100). |
| `skip` | query | `number` | no | Number of results to skip (default: 0). |
