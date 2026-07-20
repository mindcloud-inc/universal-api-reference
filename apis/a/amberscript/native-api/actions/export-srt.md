# Export SRT with Amberscript

Retrieves SRT subtitle export for an Amberscript job.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/export-srt`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Export SRT](https://amberscript.github.io/api-docs/#export-to-srt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `string` | yes | The finished job to export. |
| `maxCharsPerRow` | query | `number` | no | Maximum characters per subtitle row. |
| `maxNumberOfRows` | query | `number` | no | Maximum number of subtitle rows per caption. |
| `maxScreenTimePerRowSeconds` | query | `number` | no | Maximum number of seconds allocated to each subtitle row. |
