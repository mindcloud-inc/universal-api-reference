# Export File as WebVTT with Trint

Exports a file as WebVTT from Trint.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/webvtt/:trintId`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Export File as WebVTT](https://dev.trint.com/reference/webvtttrint-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trintId` | path | `string` | yes | The Trint file identifier to export. |
