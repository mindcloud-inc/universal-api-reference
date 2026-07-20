# Export Full Transcript as CSV with Trint

Exports a full transcript as CSV from Trint.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/csv/full/:trintId`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Export Full Transcript as CSV](https://dev.trint.com/reference/full-transcript-csv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trintId` | path | `string` | yes | The Trint file identifier to export. |
