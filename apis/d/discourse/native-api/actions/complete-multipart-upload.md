# Complete Multipart Upload with Discourse

Completes a multipart upload in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads/complete-multipart.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Complete Multipart Upload](https://docs.discourse.org/#tag/Uploads/operation/completeMultipart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parts` | body | `string` | yes | JSON array of multipart part objects with part_number and etag. |
| `unique_identifier` | body | `string` | yes | The unique identifier returned by Create Multipart Upload. |
