# Update Product with ReadyCloud Suite

Updates an existing product in ReadyCloud Suite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/orgs/:orgPk/products/:productPk/`
- **Base URL:** `https://www.readycloud.com`
- **Official documentation:** [Update Product](https://www.readycloud.com/static/api-doc/v2/02-apireference-v2-11-products.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgPk` | path | `string` | yes | ReadyCloud organization identifier. |
| `productPk` | path | `string` | yes | ReadyCloud product identifier. |
