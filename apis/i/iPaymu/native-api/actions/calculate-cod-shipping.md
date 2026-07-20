# Calculate COD Shipping with iPaymu

Calculate shipping costs for an iPaymu cash-on-delivery shipment.

## Endpoint

- **Method:** `POST`
- **Path:** `/cod/shipping-calculate`
- **Base URL:** `https://my.ipaymu.com/api/v2`
- **Official documentation:** [Calculate COD Shipping](https://ipaymu.com/api-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `destination_area_id` | body | `string` | yes | Destination area identifier. |
| `pickup_area_id` | body | `string` | yes | Pickup area identifier. |
| `weight` | body | `number` | yes | Shipment weight in kilograms. |
| `amount` | body | `number` | yes | Order amount. |
