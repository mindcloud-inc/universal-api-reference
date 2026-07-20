# List Reviews with DocuPanda - Document Understanding

Retrieves reviews from DocuPanda.

## Endpoint

- **Method:** `GET`
- **Path:** `/reviews`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [List Reviews](https://docs.docupipe.ai/reference/list_reviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_data` | query | `boolean` | no | Whether to include the data payload in the response |
| `limit` | query | `number` | no | The maximum number of reviews to return. Maximum is 1000 |
| `offset` | query | `number` | no | The number of reviews to skip (to paginate through the data) |
