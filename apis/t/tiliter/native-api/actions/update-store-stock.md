# Update Store Stock with Tiliter

Updates store stock in the Tiliter Recognition API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/stores/:store_id/stock`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Update Store Stock](https://developer.tiliter.com/reference/update_store_stock)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `store_id` | path | `string` | yes |
| `stockStates[]` | body | `array<object>` | yes |
