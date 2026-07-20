# Create Customer Order with MRPeasy

Creates a new customer order in MRPeasy.

## Endpoint

- **Method:** `POST`
- **Path:** `/customer-orders`
- **Base URL:** `https://api.mrpeasy.com/rest/v1`
- **Official documentation:** [Create Customer Order](https://www.mrpeasy.com/resources/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | body | `number` | yes | MRPeasy customer ID for the order. |
| `reference` | body | `string` | no | Optional customer order reference. |
| `products` | body | `array<object>` | yes | Array of MRPeasy order line objects, for example [{"article_id":1,"quantity":1,"item_price_cur":10}]. |
