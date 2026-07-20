# Create Or Update Review with Reloadify

Creates or updates a review in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/reviews`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Or Update Review](https://app.reloadify.com/api-docs/index.html#/reviews/putV2LanguagesLanguageIdReviews)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `review.id` | body | `string` | yes | Review identifier. |
| `review.product_id` | body | `string` | yes | Existing product ID. |
| `review.profile_id` | body | `string` | yes | Existing profile ID. |
