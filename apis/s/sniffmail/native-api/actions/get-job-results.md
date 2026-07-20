# Get Job Results with Sniffmail

Retrieves results for a bulk verification job.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:jobId/results`
- **Base URL:** `https://api.sniffmail.io`
- **Official documentation:** [Get Job Results](https://sniffmail.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Provide the Sniffmail bulk job ID returned by Create Bulk Job. |
