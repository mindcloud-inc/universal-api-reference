# Update Article with Everbill

Updates an existing article in Everbill.

## Endpoint

- **Method:** `PUT`
- **Path:** `/articles/update/:id`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Update Article](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1articles~1update{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Everbill record ID. |
| `Article` | body | `object` | yes | Article object for the request body. |
