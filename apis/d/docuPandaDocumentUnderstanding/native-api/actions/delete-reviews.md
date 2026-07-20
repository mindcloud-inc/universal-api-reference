# Delete Reviews with DocuPanda - Document Understanding

Deletes existing reviews from DocuPanda.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/reviews`
- **Base URL:** `https://app.docupipe.ai`
- **Official documentation:** [Delete Reviews](https://docs.docupipe.ai/reference/delete_reviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewIds` | body | `list<string>` | yes | Unique identifiers of the review objects to be deleted. |
