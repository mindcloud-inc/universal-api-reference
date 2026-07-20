# Download Files with pixx.io

Downloads converted files from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/convert`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [Download Files](https://api.pixxio.com/docs/openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downloadFormatID` | query | `number` | no | Download format ID when downloadType is downloadFormat. |
| `downloadType` | query | `string` | no | Download type such as original, preview, custom, or downloadFormat. |
| `fileExtension` | query | `string` | no | Output file extension for custom conversion. |
| `fileName` | query | `string` | no | Output file name. |
| `ids` | query | `number<number>` | no | File IDs to convert or download. Send multiple values as a array. |
