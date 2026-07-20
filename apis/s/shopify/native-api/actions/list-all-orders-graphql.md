# List All Orders with Shopify

Retrieves orders from Shopify with GraphQL.

## Endpoint

- **Method:** `POST`
- **Path:** `2025-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [List All Orders](https://shopify.dev/docs/api/admin-graphql/latest/queries/orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderQuery` | body | `string` | no | Optional Shopify order search query string. Leave blank to list orders. |
| `createdAfter` | body | `string` | no | Optional lower bound for Shopify created_at order search, for example 2026-03-01 or 2026-03-01T00:00:00Z. |
| `createdBefore` | body | `string` | no | Optional upper bound for Shopify created_at order search, for example 2026-04-01 or 2026-04-01T00:00:00Z. |
| `updatedAfter` | body | `string` | no | Optional lower bound for Shopify updated_at order search, for example 2026-03-01 or 2026-03-01T00:00:00Z. |
| `updatedBefore` | body | `string` | no | Optional upper bound for Shopify updated_at order search, for example 2026-04-01 or 2026-04-01T00:00:00Z. |
| `financialStatus` | body | `string` | no | Optional Shopify financial_status filter, for example paid, pending, authorized, partially_paid, refunded, or voided. |
| `names[]` | body | `array<string>` | no | Optional list of Shopify order names to match, for example #1001 or 1001. |
| `reverse` | body | `boolean` | no | Reverse the sort order of the results. |
| `afterCursor` | body | `string` | no | Optional cursor for manually continuing from a previous page. Standard pagination controls handle this automatically in most workflows. |
