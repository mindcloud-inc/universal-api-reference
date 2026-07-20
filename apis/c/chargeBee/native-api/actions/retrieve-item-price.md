# Retrieve Item Price with ChargeBee

Retrieves an item price from ChargeBee.

## Endpoint

- **Method:** `GET`
- **Path:** `item_prices/:item_price_id`
- **Base URL:** `https://{baseUrl}.chargebee.com/api/v2/`
- **Official documentation:** [Retrieve Item Price](https://apidocs.chargebee.com/docs/api/item-prices/retrieve-an-item-price)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_price_id` | path | `string` | yes | The Chargebee item price identifier. |
