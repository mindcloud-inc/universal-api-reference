# Update Offer with Everbill

Updates an existing offer in Everbill.

## Endpoint

- **Method:** `PUT`
- **Path:** `/offers/update/:id`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Update Offer](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1offers~1update~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Everbill record ID. |
| `Offer` | body | `object` | yes | Offer object for the request body. |
| `Customer` | body | `object` | yes | Customer object for the request body. |
| `Address` | body | `object` | no | Address object for the request body. |
| `Article[]` | body | `array<object>` | no | Article array for the request body. |
| `Transaction[]` | body | `array<object>` | no | Transaction array for the request body. |
