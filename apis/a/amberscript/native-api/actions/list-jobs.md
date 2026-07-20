# List Jobs with Amberscript

Retrieves jobs from your Amberscript account.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://api.amberscript.com/api`
- **Official documentation:** [List Jobs](https://amberscript.github.io/api-docs/#get-list-of-jobs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `string` | no | Return only the job with this ID. |
| `jobType` | query | `string` | no | Filter jobs by type, such as `perfect` or `direct`. |
| `status` | query | `string` | no | Filter jobs by status: `OPEN`, `ERROR`, or `DONE`. |
| `transcriptionType` | query | `string` | no | Filter jobs by transcription type, such as `transcription`. |
