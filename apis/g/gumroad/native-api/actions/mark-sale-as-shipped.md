# Mark Sale as Shipped with Gumroad

Marks a sale as shipped in Gumroad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sales/:id/mark_as_shipped`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Mark Sale as Shipped](https://gumroad.com/api#put-/sales/:id/mark_as_shipped)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The sale ID. |
| `tracking_url` | body | `string` | no | The shipment tracking URL. |
