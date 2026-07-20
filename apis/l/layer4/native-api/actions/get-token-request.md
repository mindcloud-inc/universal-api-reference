# Get Token Request with Layer4

Retrieves a token request from a Layer4 bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/token-requests/:tokenRequestId`
- **Base URL:** `https://www.layer4.app`
- **Official documentation:** [Get Token Request](https://www.layer4.app/api-docs#tag/Token-Requests/operation/TokenRequestsController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | The Layer4 bucket identifier. |
| `tokenRequestId` | path | `string` | yes | The Layer4 token request identifier. |
