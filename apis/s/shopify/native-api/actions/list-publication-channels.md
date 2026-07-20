# List Publication Channels with Shopify

Retrieves publication channels from Shopify.

## Endpoint

- **Method:** `POST`
- **Path:** `2026-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [List Publication Channels](https://shopify.dev/docs/api/admin-graphql/latest/queries/publications)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Container for Shopify GraphQL variables used by this action. |
| `variables.catalogType` | body | `string` | no | Optional Shopify catalog type filter. Accepted values: `0`, `1`, `2`. |
| `variables.first` | body | `number` | no | Max publication channels to return in a single call. |
| `variables.after` | body | `string` | no | Optional cursor for manually fetching the next page. |
