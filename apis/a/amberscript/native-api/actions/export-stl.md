# Export STL with Amberscript

Retrieves STL subtitle export for an Amberscript job.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/export-stl`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Export STL](https://amberscript.github.io/api-docs/#export-to-stl)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `string` | yes | The finished job to export. |
| `maxNumberOfRows` | query | `number` | no | Maximum number of subtitle rows per caption. |
| `maxScreenTimePerRowSeconds` | query | `number` | no | Maximum number of seconds allocated to each subtitle row. |
