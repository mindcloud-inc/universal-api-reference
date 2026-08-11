# Set Fixed Price on Price List with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [Set Fixed Price on Price List](https://shopify.dev/docs/api/admin-graphql/latest/mutations/pricelistfixedpricesadd)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `priceListId` | body | `list` | yes | Select the Shopify price list that should receive the fixed variant price. |
| `variantId` | body | `string` | yes | Shopify ProductVariant GID whose catalog price will be set. |
| `amount` | body | `number` | yes | Absolute fixed price amount for the variant. |
| `currencyCode` | body | `list<string>` | yes | Currency code matching the price list currency. |
