# GraphQL - Get Records (Paginated) with Shopify

Retrieves records from Shopify with paginated GraphQL queries.

## Endpoint

- **Method:** `POST`
- **Path:** `:version/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [GraphQL - Get Records (Paginated)](https://shopify.dev/docs/api/admin-graphql/latest)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | body | `string` | no |
| `variables` | body | `object` | no |
| `version` | path | `string` | no |
