# Get Batch Verification Job with ClearBounce

Retrieves a batch verification job from ClearBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/status/:jobId`
- **Base URL:** `https://api.clearbounce.net/api/v1`
- **Official documentation:** [Get Batch Verification Job](https://docs.clearbounce.net/api-reference/batch-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The batch verification job ID returned by the upload step. |
