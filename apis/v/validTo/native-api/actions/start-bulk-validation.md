# Start Bulk Validation with validTo

Starts a bulk validation list in validTo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bulk/:jobId`
- **Base URL:** `https://api.validto.com/v1`
- **Official documentation:** [Start Bulk Validation](https://validto.readme.io/reference/verify-a-bulk-validation-list)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The bulk validation job ID. |
