# Update a Review with DocuPanda - Document Understanding

Updates an existing review in DocuPanda.

## Endpoint

- **Method:** `POST`
- **Path:** `/review/:review_id/update`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Update a Review](https://docs.docupipe.ai/reference/update_review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | The data to update the review with. This should be a dictionary with the same structure as the review object. If omitted, the data will not be updated. |
| `review_id` | path | `string` | yes | — |
| `reviewStatus` | body | `string` | yes | — |
