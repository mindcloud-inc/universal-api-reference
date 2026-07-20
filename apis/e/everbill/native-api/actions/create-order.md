# Create Order with Everbill

Creates a new order in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/orders/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Order](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1orders~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Order` | body | `object` | yes | Order object for the request body. |
| `Distributor` | body | `object` | yes | Distributor object for the request body. |
| `Article[]` | body | `array<object>` | no | Article array for the request body. |
| `Transaction[]` | body | `array<object>` | no | Transaction array for the request body. |
