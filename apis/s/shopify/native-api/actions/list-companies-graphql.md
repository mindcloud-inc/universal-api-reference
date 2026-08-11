# List Companies with Shopify

Retrieves companies from Shopify with GraphQL.

## Endpoint

- **Method:** `POST`
- **Path:** `2026-07/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** GraphQL
- **Official documentation:** [List Companies](https://shopify.dev/docs/api/admin-graphql/2026-07/queries/companies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyQuery` | body | `string` | no | Optional Shopify company search query string. Leave blank to list companies. |
| `externalId` | body | `string` | no | Find the Shopify B2B company whose externalId matches this external source-system ID. |
| `createdAfter` | body | `string` | no | Optional lower bound for Shopify created_at company search, for example 2026-03-01 or 2026-03-01T00:00:00Z. |
| `createdBefore` | body | `string` | no | Optional upper bound for Shopify created_at company search, for example 2026-04-01 or 2026-04-01T00:00:00Z. |
| `updatedAfter` | body | `string` | no | Optional lower bound for Shopify updated_at company search, for example 2026-03-01 or 2026-03-01T00:00:00Z. |
| `updatedBefore` | body | `string` | no | Optional upper bound for Shopify updated_at company search, for example 2026-04-01 or 2026-04-01T00:00:00Z. |
| `afterCursor` | body | `string` | no | Optional cursor for manually continuing from a previous page. Standard pagination controls handle this automatically in most workflows. |
