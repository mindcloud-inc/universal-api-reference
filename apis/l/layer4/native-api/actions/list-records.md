# List Records with Layer4

Retrieves records from a Layer4 bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/records`
- **Base URL:** `https://www.layer4.app`
- **Official documentation:** [List Records](https://www.layer4.app/api-docs#tag/Records/operation/RecordsController_findAll)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | The Layer4 bucket identifier. |
| `segmentId` | query | `string` | no | Filter records by segment. |
| `decrypt` | query | `boolean` | no | Return decrypted records when available. |
