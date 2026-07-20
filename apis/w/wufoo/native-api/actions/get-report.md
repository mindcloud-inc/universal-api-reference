# Get Report with Wufoo

Retrieves a report from Wufoo by identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:identifier.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [Get Report](https://wufoo.github.io/docs/#reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The report hash or identifier to retrieve. |
