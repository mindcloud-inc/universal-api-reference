# Create Purchase Event with Reloadify

Creates a server-side purchase event in Reloadify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/languages/:language_id/purchase_events`
- **Base URL:** `https://api.reloadify.com/api`
- **Official documentation:** [Create Purchase Event](https://app.reloadify.com/api-docs/index.html#/purchase_events/putV2LanguagesLanguageIdPurchaseEvents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_id` | path | `string` | yes | Reloadify language ID. |
| `purchase_event.order_id` | body | `string` | yes | Existing order ID. |
| `purchase_event.profile_id` | body | `string` | yes | Existing profile ID. |
| `purchase_event.visitor_token` | body | `string` | yes | Reloadify tracking visitor token. |
