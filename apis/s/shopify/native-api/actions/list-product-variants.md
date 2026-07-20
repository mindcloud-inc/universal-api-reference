# List Product Variants with Shopify

Retrieves product variants from Shopify.

## Endpoint

- **Method:** `POST`
- **Path:** `2026-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [List Product Variants](https://shopify.dev/docs/api/admin-graphql/latest/queries/productVariants)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Shopify product variant search query. Leave blank to list variants, or enter any supported productVariants search query such as sku, barcode, product_id, product_status, or updated_at. |
| `updatedAfter` | body | `string` | no | Optional modified-date lower bound for Shopify variant search. Appends updated_at:>= to the Product Variant Query. Use YYYY-MM-DD or an ISO timestamp. |
| `updatedBefore` | body | `string` | no | Optional modified-date upper bound for Shopify variant search. Appends updated_at:<= to the Product Variant Query. Use YYYY-MM-DD or an ISO timestamp. |
| `afterCursor` | body | `string` | no | Pass previous page endCursor to fetch the next page. |
| `metafieldKeys` | body | `string` | no | Optional comma-separated Shopify metafield keys in namespace.key format. When provided, matching metafields are returned for both the variant and its parent product. |
