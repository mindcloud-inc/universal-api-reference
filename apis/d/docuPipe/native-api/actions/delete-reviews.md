# Delete Reviews with DocuPipe

Deletes reviews from DocuPipe.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/reviews`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Delete Reviews](https://docs.docupipe.ai/reference/delete_reviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewIds[]` | body | `array<string>` | yes | Unique identifiers of the review objects to be deleted. |
