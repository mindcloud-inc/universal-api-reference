# Create Incoming Bill with Everbill

Creates a new incoming bill in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/incoming_bills/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Incoming Bill](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1incoming_bills~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IncomingBill` | body | `object` | yes | IncomingBill object for the request body. |
| `Distributor` | body | `object` | yes | Distributor object for the request body. |
| `Article[]` | body | `array<object>` | no | Article array for the request body. |
| `Discount[]` | body | `array<object>` | no | Discount array for the request body. |
| `Transaction[]` | body | `array<object>` | no | Transaction array for the request body. |
