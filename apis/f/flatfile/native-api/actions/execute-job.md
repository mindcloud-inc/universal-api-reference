# Execute Job with Flatfile

Executes a specific job in Flatfile.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:jobId/execute`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Execute Job](https://reference.flatfile.com/api-reference/jobs/execute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Flatfile job identifier. |
