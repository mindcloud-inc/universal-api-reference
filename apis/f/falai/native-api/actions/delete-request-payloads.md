# Delete Request Payloads with fal.ai

Deletes fal.ai request payloads and output files.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/models/requests/:requestId/payloads`
- **Base URL:** `https://api.fal.ai/v1`
- **Official documentation:** [Delete Request Payloads](https://fal.ai/docs/api-reference/platform-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | fal.ai request ID whose payloads should be deleted. |
