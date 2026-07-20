# Batch Presign Multipart Parts with Discourse

Generates presigned URLs for multipart upload parts in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/batch-presign-multipart-parts.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Batch Presign Multipart Parts](https://docs.discourse.org/#tag/Uploads/operation/batchPresignMultipartParts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `part_numbers` | body | `string` | yes | Multipart part numbers to presign. |
| `unique_identifier` | body | `string` | yes | The unique identifier returned by Create Multipart Upload. |
