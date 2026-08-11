# Create or Update Product with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [Create or Update Product](https://shopify.dev/docs/api/admin-graphql/2026-07/mutations/productSet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | body | `string` | yes | Product handle used as the create-or-update identifier. |
| `title` | body | `string` | yes | Product title. Required so the same action can create a missing product. |
| `sku` | body | `string` | yes | SKU for the product's single default variant. |
| `price` | body | `number` | yes | Base price for the product's single default variant. |
| `tracked` | body | `boolean` | yes | Whether Shopify tracks inventory for the variant. |
| `requiresShipping` | body | `boolean` | yes | Whether the variant requires shipping. |
| `inventoryPolicy` | body | `list<string>` | yes | Behavior when inventory reaches zero. Accepted values: `CONTINUE`, `DENY`. |
| `locationId` | body | `list` | yes | Shopify location GID where available inventory is set. |
| `quantity` | body | `number` | yes | Available inventory quantity at the selected location. |
