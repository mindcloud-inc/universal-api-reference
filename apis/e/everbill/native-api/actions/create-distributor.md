# Create Distributor with Everbill

Creates a new distributor in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/distributors/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Distributor](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1distributors~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Distributor` | body | `object` | yes | Distributor object for the request body. |
| `Contact` | body | `object` | no | Contact object for the request body. |
