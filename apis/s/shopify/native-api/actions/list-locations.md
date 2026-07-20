# List Locations with Shopify

Retrieves locations from Shopify.

## Endpoint

- **Method:** `POST`
- **Path:** `2026-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [List Locations](https://shopify.dev/docs/api/admin-graphql/latest/queries/locations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `locationQuery` | body | `string` | no | Optional raw Shopify locations query string, such as `name:Online` or `id:>=69379358899`. |
| `afterCursor` | body | `string` | no | Optional cursor from the previous page to fetch the next page of locations. |
