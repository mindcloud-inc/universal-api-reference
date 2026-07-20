# Update Review Request with gotoHuman

Updates an existing review request in gotoHuman.

## Endpoint

- **Method:** `POST`
- **Path:** `/requestReview`
- **Base URL:** `https://api.gotohuman.com`
- **Official documentation:** [Update Review Request](https://docs.gotohuman.com/retries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `updateForReviewId` | body | `string` | yes | The review ID to update. |
| `formId` | body | `string` | yes | The ID of the review template / form. |
| `fields` | body | `string` | yes | JSON object of updated field values for the review request. |
| `assignToGroups` | body | `string` | no | JSON array string of reviewer group IDs. |
