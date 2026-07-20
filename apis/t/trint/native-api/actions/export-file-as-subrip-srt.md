# Export File as SubRip SRT with Trint

Exports a file as SubRip SRT from Trint.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/srt/:trintId`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Export File as SubRip SRT](https://dev.trint.com/reference/testinput-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trintId` | path | `string` | yes | The Trint file identifier to export. |
