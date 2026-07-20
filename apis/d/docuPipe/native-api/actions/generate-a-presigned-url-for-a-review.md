# Generate a Presigned URL for a Review with DocuPipe

Retrieves a presigned review URL from DocuPipe.

## Endpoint

- **Method:** `GET`
- **Path:** `/review/:reviewId/presigned-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Generate a Presigned URL for a Review](https://docs.docupipe.ai/reference/get_presigned_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `review_id` | path | `string` | yes | — |
| `expiry_hours` | query | `number` | no | How many hours the presigned URL should remain valid. If omitted, the link will never expire. |
