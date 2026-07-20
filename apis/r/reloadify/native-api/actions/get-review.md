# Get Review with Reloadify

Retrieves a review from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/reviews/:review_id`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Get Review](https://app.reloadify.com/api-docs/index.html#/reviews/getV2LanguagesLanguageIdReviewsReviewId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `review_id` | path | `string` | yes | Review identifier. |
