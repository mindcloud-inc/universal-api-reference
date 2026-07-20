# List Report Fields with Wufoo

Retrieves fields from a specific Wufoo report.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:identifier/fields.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [List Report Fields](https://wufoo.github.io/docs/#reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The report hash or identifier whose fields to retrieve. |
