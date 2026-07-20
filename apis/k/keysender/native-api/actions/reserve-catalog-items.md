# Reserve Catalog Items with Keysender

Creates a catalog reservation in Keysender.

## Endpoint

- **Method:** `POST`
- **Path:** `/catalog/reserve`
- **Base URL:** `https://panel.keysender.co.uk/api/v1.0`
- **Official documentation:** [Reserve Catalog Items](https://panel.keysender.co.uk/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `string` | no | — |
| `order_items` | body | `object<object>` | yes | Array of reservation line items with sku and quantity. Send multiple values as a array. |
