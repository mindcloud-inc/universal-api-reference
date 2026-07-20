# Acknowledge Job with Flatfile

Acknowledges a specific job in Flatfile.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/:jobId/ack`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Acknowledge Job](https://reference.flatfile.com/api-reference/jobs/ack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Flatfile job identifier. |
