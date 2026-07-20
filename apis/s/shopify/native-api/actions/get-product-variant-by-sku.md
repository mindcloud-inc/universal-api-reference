# Get Product Variant by SKU with Shopify

Finds product variants in Shopify by SKU.

## Endpoint

- **Method:** `POST`
- **Path:** `2026-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [Get Product Variant by SKU](https://shopify.dev/docs/api/admin-graphql/latest/queries/productVariants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | — |
| `query` | body | `string` | no | A GraphQL query to find a product by it's SKU. |
| `variables.query` | body | `string` | yes | Exact Shopify SKU. The action automatically applies Shopify's sku: search filter. |
