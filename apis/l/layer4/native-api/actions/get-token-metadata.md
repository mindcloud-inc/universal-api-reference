# Get Token Metadata with Layer4

Retrieves the metadata of a Layer4 token.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/tokens/:tokenId/metadata`
- **Base URL:** `https://www.layer4.app`
- **Official documentation:** [Get Token Metadata](https://www.layer4.app/api-docs#tag/Tokens/operation/TokensController_findMetadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | The Layer4 bucket identifier. |
| `tokenId` | path | `string` | yes | The Layer4 token identifier. |
