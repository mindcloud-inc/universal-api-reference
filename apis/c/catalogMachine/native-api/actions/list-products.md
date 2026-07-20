# List Products with Catalog Machine

Retrieves all products from Catalog Machine.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [List Products](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Filter products by category name. |
| `collection` | query | `string` | no | Filter products by collection name. |
