# Get Record Request with Layer4

Retrieves a record request from a Layer4 bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/record-requests/:recordRequestId`
- **Base URL:** `https://www.layer4.app`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Layer4 bucket ID. |
| `decrypt` | query | `boolean` | no | Whether to decrypt the record request. |
| `recordRequestId` | path | `string` | yes | Layer4 record request ID. |
