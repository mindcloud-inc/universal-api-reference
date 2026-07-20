# Export TXT with Amberscript

Retrieves plain text export for an Amberscript job.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/export-txt`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Export TXT](https://amberscript.github.io/api-docs/#export-to-text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `string` | yes | The finished job to export. |
| `includeTimestamps` | query | `boolean` | no | Include timestamps in the exported text. |
| `includeSpeakers` | query | `boolean` | no | Include speaker labels in the exported text. |
| `highlightsOnly` | query | `boolean` | no | Return only highlighted transcript segments. |
| `maxCharsPerRow` | query | `number` | no | Maximum number of characters per row. |
