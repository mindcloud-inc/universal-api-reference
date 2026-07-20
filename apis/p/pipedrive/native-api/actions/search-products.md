# Search Products with Pipedrive

Finds products in Pipedrive by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/products/search`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Search Products](https://developers.pipedrive.com/docs/api/v1/Products)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | yes | Search term for products. |
| `exact_match` | query | `boolean` | no | Set true to only return exact matches. |
| `limit` | query | `number` | no | Max number of results to return. |
| `cursor` | query | `string` | no | Pagination cursor from previous response. |
