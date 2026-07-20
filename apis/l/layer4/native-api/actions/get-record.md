# Get Record with Layer4

Retrieves a record from a Layer4 bucket.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/buckets/:bucketId/records/:recordId`
- **Base URL:** `https://www.layer4.app`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Layer4 bucket ID. |
| `decrypt` | query | `boolean` | no | Whether to decrypt the record. |
| `recordId` | path | `string` | yes | Layer4 record ID. |
