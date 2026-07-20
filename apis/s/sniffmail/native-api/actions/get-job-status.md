# Get Job Status with Sniffmail

Retrieves the status of a bulk verification job.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:jobId`
- **Base URL:** `https://api.sniffmail.io`
- **Official documentation:** [Get Job Status](https://sniffmail.io/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Provide the Sniffmail bulk job ID returned by Create Bulk Job. |
