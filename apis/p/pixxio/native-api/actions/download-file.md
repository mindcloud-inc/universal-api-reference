# Download File with pixx.io

Downloads a converted file from your pixx.io workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/files/:id/convert`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [Download File](https://api.pixxio.com/docs/openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downloadFormatID` | query | `number` | no | Download format ID when downloadType is downloadFormat. |
| `downloadType` | query | `string` | no | Download type such as original, preview, custom, or downloadFormat. |
| `fileExtension` | query | `string` | no | Output file extension for custom conversion. |
| `height` | query | `number` | no | Requested output height for custom conversion. |
| `id` | path | `number` | yes | The pixx.io file ID to download or convert. |
| `width` | query | `number` | no | Requested output width for custom conversion. |
