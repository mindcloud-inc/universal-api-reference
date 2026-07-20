# Request COD Pickup with iPaymu

Create an iPaymu cash-on-delivery pickup request.

## Endpoint

- **Method:** `POST`
- **Path:** `/cod/pickup`
- **Base URL:** `https://my.ipaymu.com/api/v2`
- **Official documentation:** [Request COD Pickup](https://ipaymu.com/api-collection/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | body | `string` | yes | COD transaction identifier. |
| `pickup_date` | body | `string` | yes | Pickup date in YYYY-MM-DD. |
| `pickup_time` | body | `string` | yes | Pickup time in HH:mm. |
| `pickup_vehicle` | body | `string` | yes | Pickup vehicle, for example Motor or Mobil. |
