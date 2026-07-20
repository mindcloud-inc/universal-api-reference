# List Reviews for a Reviewer Group with Filestage

Retrieves reviews for a Filestage reviewer group.

## Endpoint

- **Method:** `GET`
- **Path:** `/steps/{stepId}/reviews`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [List Reviews for a Reviewer Group](https://developers.filestage.io/docs/api/a1b2c3d4e5f6g-get-reviews-for-a-review-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stepId` | path | `string` | yes | The unique identifier of the Review Group. |
| `limit` | query | `number` | no | The maximum number of reviews to return. Defaults to 20. |
| `orderBy` | query | `string` | no | The order in which to sort the reviews. |
| `pageToken` | query | `string` | no | A token to retrieve the next page of results. |
