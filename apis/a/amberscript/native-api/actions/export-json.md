# Export JSON with Amberscript

Retrieves JSON export for an Amberscript job.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/export-json`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [Export JSON](https://amberscript.github.io/api-docs/#export-to-json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `string` | yes | The finished job to export. |
