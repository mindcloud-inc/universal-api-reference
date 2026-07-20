# List Rates with Ship&Co

## Endpoint

- **Method:** `POST`
- **Path:** `/rates`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [List Rates](https://developer.shipandco.com/en/#rates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `setup` | body | `object` | yes | Carrier and rate setup details. Do not include service for rates. |
| `to_address` | body | `object` | yes | Recipient address object. |
| `from_address` | body | `object` | yes | Sender address object. |
| `products[]` | body | `array<object>` | yes | Product line items array. |
| `parcels[]` | body | `array<object>` | yes | Parcel details array. |
| `customs` | body | `object` | no | Customs details for international rate requests. |
