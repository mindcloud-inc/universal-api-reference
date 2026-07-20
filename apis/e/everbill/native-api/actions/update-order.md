# Update Order with Everbill

Updates an existing order in Everbill.

## Endpoint

- **Method:** `PUT`
- **Path:** `/orders/update/:id`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Update Order](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1orders~1update~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Everbill record ID. |
| `Order` | body | `object` | yes | Order object for the request body. |
| `Distributor` | body | `object` | yes | Distributor object for the request body. |
| `Article[]` | body | `array<object>` | no | Article array for the request body. |
| `Transaction[]` | body | `array<object>` | no | Transaction array for the request body. |
