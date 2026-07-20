# Create Shipment with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/shipments`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [Create Shipment](https://developer.shipandco.com/en/#shipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setup` | body | `object` | yes | Carrier, service, and shipping setup details. |
| `to_address` | body | `object` | yes | Recipient address object. |
| `from_address` | body | `object` | yes | Sender address object. |
| `products[]` | body | `array<object>` | yes | Product line items array. |
| `parcels[]` | body | `array<object>` | no | Parcel details array for international shipping. |
| `customs` | body | `object` | no | Customs details for international shipments. |
