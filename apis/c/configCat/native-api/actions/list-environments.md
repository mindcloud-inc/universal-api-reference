# List Environments with ConfigCat

Retrieves a list of environments from ConfigCat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/products/:productId/environments`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [List Environments](https://configcat.com/docs/api/reference/get-environments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | The identifier of the Product. |
