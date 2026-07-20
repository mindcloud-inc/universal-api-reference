# Get Token with Layer4

Retrieves a token from a Layer4 bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/tokens/:tokenId`
- **Base URL:** `https://www.layer4.app`
- **Official documentation:** [Get Token](https://www.layer4.app/api-docs#tag/Tokens/operation/TokensController_findOne)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | The Layer4 bucket identifier. |
| `tokenId` | path | `string` | yes | The Layer4 token identifier. |
