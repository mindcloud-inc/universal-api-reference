# List Sales Data with Deputy

Retrieves raw sales metrics from Deputy.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/metrics/raw`
- **Base URL:** `https://{endpoint}.deputy.com`
- **Official documentation:** [List Sales Data](https://developer.deputy.com/docs/retrieving-sales-data-from-deputy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `areas` | query | `string` | yes | Comma-separated Deputy area IDs. |
| `end` | query | `number` | yes | Unix timestamp for the end of the reporting window. |
| `start` | query | `number` | yes | Unix timestamp for the start of the reporting window. |
| `types` | query | `string` | yes | Comma-separated metric types, for example Sales or Transactions. |
