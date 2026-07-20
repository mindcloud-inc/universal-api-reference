# Get Products with Pipedrive

Retrieves products from Pipedrive.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/products`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Get Products](https://developers.pipedrive.com/docs/api/v1/Products)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Max number of products to return. |
| `cursor` | query | `string` | no | Pagination cursor from previous response. |
