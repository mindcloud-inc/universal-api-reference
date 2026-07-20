# List Global Unsubscribes with Reloadify

Retrieves global unsubscribes from Reloadify.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/languages/:language_id/global_unsubscribes`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [List Global Unsubscribes](https://app.reloadify.com/api-docs/index.html#/global_unsubscribes/getV2LanguagesLanguageIdGlobalUnsubscribes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `string` | no | Only include global unsubscriptions created after this timestamp. |
| `created_before` | query | `string` | no | Only include global unsubscriptions created before this timestamp. |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `updated_after` | query | `string` | no | Only include global unsubscriptions updated after this timestamp. |
| `updated_before` | query | `string` | no | Only include global unsubscriptions updated before this timestamp. |
