# Create Customer with Everbill

Creates a new customer in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Customer](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1customers~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Customer` | body | `object` | yes | Customer object for the request body. |
| `Contact` | body | `object` | no | Contact object for the request body. |
| `Address` | body | `object` | no | Address object for the request body. |
