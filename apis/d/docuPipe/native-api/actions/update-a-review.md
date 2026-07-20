# Update a Review with DocuPipe

Updates a review in DocuPipe.

## Endpoint

- **Method:** `POST`
- **Path:** `/review/:reviewId/update`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update a Review](https://docs.docupipe.ai/reference/update_review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `review_id` | path | `string` | yes | — |
| `data` | body | `object` | no | The data to update the review with. This should be a dictionary with the same structure as the review object. If omitted, the data will not be updated. |
| `reviewStatus` | body | `list` | yes | Use this field to indicate whether the posted object is verified to be correct, incorrect, or not yet fully verified. Accepted values: `rejected`, `unverified`, `verified`. |
