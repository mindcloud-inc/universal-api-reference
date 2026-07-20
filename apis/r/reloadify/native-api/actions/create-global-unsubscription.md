# Create Global Unsubscription with Reloadify

Creates a global unsubscription in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/global_unsubscribes`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Global Unsubscription](https://app.reloadify.com/api-docs/index.html#/global_unsubscribes/putV2LanguagesLanguageIdGlobalUnsubscribes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `global_unsubscribe.email` | body | `string` | yes | Email to unsubscribe globally. |
| `global_unsubscribe.unsubscribed` | body | `boolean` | yes | Whether the address is unsubscribed globally. |
