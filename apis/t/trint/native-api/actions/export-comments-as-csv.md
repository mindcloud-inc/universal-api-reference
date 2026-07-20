# Export Comments as CSV with Trint

Exports file comments as CSV from Trint.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/csv/comments/:trintId`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Export Comments as CSV](https://dev.trint.com/reference/csvcommentstrint-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trintId` | path | `string` | yes | The Trint file identifier to export. |
