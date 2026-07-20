# List Products with Shopify

Retrieves products from Shopify with GraphQL.

## Endpoint

- **Method:** `POST`
- **Path:** `2026-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [List Products](https://shopify.dev/docs/api/admin-graphql/latest/queries/products)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Shopify product search query. Defaults to active products only. |
| `afterCursor` | body | `string` | no | Pass previous page endCursor to fetch the next page. |
| `metafieldKeys` | body | `string` | no | Optional comma-separated Shopify metafield keys in namespace.key format. When provided, matching metafields are returned for both the product and its variants. |
