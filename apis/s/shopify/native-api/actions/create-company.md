# Create Company with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [Create Company](https://shopify.dev/docs/api/admin-graphql/2026-07/mutations/companyCreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyName` | body | `string` | yes | The Shopify B2B company name. |
| `externalId` | body | `string` | yes | The external source-system ID stored in Shopify Company.externalId. |
