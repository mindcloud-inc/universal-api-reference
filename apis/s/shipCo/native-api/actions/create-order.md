# Create Order with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/orders`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Create Order](https://developer.shipandco.com/en/#order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setup` | body | `object` | yes | Carrier and shipping setup details. |
| `to_address` | body | `object` | yes | Recipient address object. |
| `products[]` | body | `array<object>` | yes | Product line items array. |
| `parcels[]` | body | `array<object>` | no | Parcel details array for international shipping. |
| `customs` | body | `object` | no | Customs details for international shipments. |
