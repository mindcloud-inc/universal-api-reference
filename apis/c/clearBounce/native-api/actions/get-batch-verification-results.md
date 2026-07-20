# Get Batch Verification Results with ClearBounce

Retrieves JSON batch verification results from ClearBounce.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/results/:jobId`
- **Base URL:** `https://api.clearbounce.net/api/v1`
- **Official documentation:** [Get Batch Verification Results](https://docs.clearbounce.net/api-reference/batch-verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The batch verification job ID returned by the upload step. |
| `status` | query | `list<string>` | no | Optional equality selector for a single verification status. Accepted values: `all`, `deliverable`, `risky`, `undeliverable`, `unknown`. |
