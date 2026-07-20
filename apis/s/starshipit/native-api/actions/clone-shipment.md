# Clone Shipment with Starshipit

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/shipment/clone`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Clone Shipment](https://api-docs.starshipit.com/#83579b84-5333-4693-93d3-85d6b52f8e5b)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `order_id` | body | `number` | no |
| `to_return_shipment` | body | `string` | no |
