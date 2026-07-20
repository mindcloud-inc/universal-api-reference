# List Purchases with Themeforest

Retrieves Envato purchases for the connected account.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/market/buyer/list-purchases`
- **Base URL:** `https://api.envato.com`
- **Official documentation:** [List Purchases](https://build.envato.com/api/#market_0_getBuyerListPurchases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_by` | query | `string` | no | Optional Envato purchase list filter. |
| `page` | query | `number` | no | Purchase result page number. |
| `include_all_item_details` | query | `boolean` | no | Whether Envato should include all item details for each purchase. |
