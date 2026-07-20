# Export Markers as CSV with Trint

Exports file markers as CSV from Trint.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/csv/markers/:trintId`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Export Markers as CSV](https://dev.trint.com/reference/markers-csv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trintId` | path | `string` | yes | The Trint file identifier to export. |
