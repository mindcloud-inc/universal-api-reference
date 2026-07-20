# Get Product Review Info with Revi.io Reviews

Retrieves product review info from Revi.io Reviews.

## Endpoint

- **Method:** `GET`
- **Path:** `/product_info`
- **Base URL:** `https://api.revi.io/api/v1`
- **Official documentation:** [Get Product Review Info](https://docs.revi7.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_product` | query | `string` | yes | The product ID to inspect. |
| `id_store` | query | `string` | no | Marketplace store ID when querying marketplace data. |
