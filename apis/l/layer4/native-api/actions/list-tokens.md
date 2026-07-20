# List Tokens with Layer4

Retrieves tokens from a Layer4 bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/tokens`
- **Base URL:** `https://www.layer4.app`
- **Official documentation:** [List Tokens](https://www.layer4.app/api-docs#tag/Tokens/operation/TokensController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | The Layer4 bucket identifier. |
| `segmentId` | query | `string` | no | Filter tokens by segment. |
