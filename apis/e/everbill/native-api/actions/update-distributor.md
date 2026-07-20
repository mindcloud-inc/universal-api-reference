# Update Distributor with Everbill

Updates an existing distributor in Everbill.

## Endpoint

- **Method:** `PUT`
- **Path:** `/distributors/update/:id`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Update Distributor](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1distributors~1update~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Everbill record ID. |
| `Distributor` | body | `object` | yes | Distributor object for the request body. |
| `Contact` | body | `object` | no | Contact object for the request body. |
