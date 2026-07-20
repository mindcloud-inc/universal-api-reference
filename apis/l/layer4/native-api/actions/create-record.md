# Create Record with Layer4

Creates a new record in a Layer4 bucket.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/buckets/:bucketId/records`
- **Base URL:** `https://www.layer4.app`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Layer4 bucket ID. |
| `contentType` | body | `string` | no | Optional content type. |
| `data` | body | `string` | yes | Record data to log on-chain. |
| `encrypt` | body | `boolean` | no | Whether to encrypt the data. |
| `segmentId` | body | `string` | no | Optional segment ID. |
