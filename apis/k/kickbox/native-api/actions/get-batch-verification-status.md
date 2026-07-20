# Get Batch Verification Status with Kickbox

Retrieves a batch verification job from Kickbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/verify-batch/:jobId`
- **Base URL:** `https://api.kickbox.com/v2`
- **Official documentation:** [Get Batch Verification Status](https://docs.kickbox.com/docs/batch-verification-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The batch verification job ID returned when the batch job was created. |
