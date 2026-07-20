# Create Token with Layer4

Creates a new token in a Layer4 bucket.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/buckets/:bucketId/tokens`
- **Base URL:** `https://www.layer4.app`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bucketId` | path | `string` | yes | Layer4 bucket ID. |
| `metadata` | body | `object` | no | Optional token metadata object. |
| `segmentId` | body | `string` | no | Optional segment ID. |
| `supply` | body | `string` | yes | Initial token supply. |
| `toAddress` | body | `string` | no | Optional recipient address or email. |
