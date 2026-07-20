# List Report Widgets with Wufoo

Retrieves widgets from a specific Wufoo report.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/:identifier/widgets.json`
- **Base URL:** `https://{subdomain}.wufoo.com/api/v3`
- **Official documentation:** [List Report Widgets](https://wufoo.github.io/docs/#reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The report hash or identifier whose widgets to retrieve. |
