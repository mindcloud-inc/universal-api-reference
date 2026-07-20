# List Deleted Product Events with Shopify

Retrieves deleted product events from Shopify.

## Endpoint

- **Method:** `POST`
- **Path:** `2026-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [List Deleted Product Events](https://shopify.dev/docs/api/admin-graphql/unstable/queries/events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Shopify event search query. Defaults to deleted product events only and can be narrowed with created_at filters. |
