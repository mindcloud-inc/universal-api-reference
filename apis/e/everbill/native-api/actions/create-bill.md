# Create Bill with Everbill

Creates a new bill in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/bills/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Bill](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Bill` | body | `object` | yes | Bill object for the request body. |
| `Customer` | body | `object` | yes | Customer object for the request body. |
| `Address` | body | `object` | no | Address object for the request body. |
| `Article[]` | body | `array<object>` | no | Article array for the request body. |
| `Discount[]` | body | `array<object>` | no | Discount array for the request body. |
| `Transaction[]` | body | `array<object>` | no | Transaction array for the request body. |
