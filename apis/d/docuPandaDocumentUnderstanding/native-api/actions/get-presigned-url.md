# Generate a Presigned URL for a Review with DocuPanda - Document Understanding

Retrieves a presigned review URL from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/review/:review_id/presigned-url`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Generate a Presigned URL for a Review](https://docs.docupipe.ai/reference/get_presigned_url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expiry_hours` | query | `number` | no | How many hours the presigned URL should remain valid. If omitted, the link will never expire. |
| `review_id` | path | `string` | yes | — |
