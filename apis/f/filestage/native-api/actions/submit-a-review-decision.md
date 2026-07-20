# Submit a Review Decision with Filestage

Submits a review decision in Filestage.

## Endpoint

- **Method:** `POST`
- **Path:** `/review/decision`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Submit a Review Decision](https://developers.filestage.io/docs/api/jsdjk349i23dl-submit-a-review-decision)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reviewId` | body | `string` | yes | The unique identifier for the review. |
| `decision` | body | `string` | yes | The decision to be submitted. |
