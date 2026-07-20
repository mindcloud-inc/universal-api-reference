# Retrieve Purchase Order with Katana

Retrieves a purchase order by ID from Katana.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchase_orders/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Retrieve Purchase Order](https://developer.katanamrp.com/reference/getpurchaseorder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Purchase order id |
| `extend[]` | query | `array<string>` | no | Array of objects that need to be added to the response |
