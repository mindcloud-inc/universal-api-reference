# Export Highlights as CSV with Trint

Exports file highlights as CSV from Trint.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/csv/highlights/:trintId`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Export Highlights as CSV](https://dev.trint.com/reference/csvhighlightstrint-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trintId` | path | `string` | yes | The Trint file identifier to export. |
