# Update Bill with Everbill

Updates an existing bill in Everbill.

## Endpoint

- **Method:** `PUT`
- **Path:** `/bills/update/:id`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Update Bill](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1bills~1update~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Everbill record ID. |
| `Bill` | body | `object` | yes | Bill object for the request body. |
| `Customer` | body | `object` | yes | Customer object for the request body. |
| `Address` | body | `object` | no | Address object for the request body. |
| `Article[]` | body | `array<object>` | no | Article array for the request body. |
| `Discount[]` | body | `array<object>` | no | Discount array for the request body. |
| `Transaction[]` | body | `array<object>` | no | Transaction array for the request body. |
