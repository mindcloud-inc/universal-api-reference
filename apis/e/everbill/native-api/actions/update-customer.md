# Update Customer with Everbill

Updates an existing customer in Everbill.

## Endpoint

- **Method:** `PUT`
- **Path:** `/customers/update/:id`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Update Customer](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1customers~1update~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Everbill record ID. |
| `Customer` | body | `object` | yes | Customer object for the request body. |
| `Contact` | body | `object` | no | Contact object for the request body. |
| `Address` | body | `object` | no | Address object for the request body. |
