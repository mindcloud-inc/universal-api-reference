# List Reviews with Reloadify

Retrieves reviews from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/reviews`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Reviews](https://app.reloadify.com/api-docs/index.html#/reviews/getV2LanguagesLanguageIdReviews)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only include reviews created after this timestamp. |
| `created_before` | query | `string` | no | Only include reviews created before this timestamp. |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `updated_after` | query | `string` | no | Only include reviews updated after this timestamp. |
| `updated_before` | query | `string` | no | Only include reviews updated before this timestamp. |
