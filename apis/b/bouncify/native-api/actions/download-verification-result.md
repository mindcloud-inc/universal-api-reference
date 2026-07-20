# Download Verification Result with Bouncify

Downloads a bulk verification result from Bouncify.

## Endpoint

- **Method:** `POST`
- **Path:** `/download`
- **Base URL:** `https://api.bouncify.io/v1`
- **Official documentation:** [Download Verification Result](https://bouncify.io/docs/api-docs/bulk-validation/download-result/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | query | `string` | yes | Bulk verification job id to download. |
| `filterResult` | body | `string` | no | Optional result categories to include in the download. Send multiple values as a array. |
