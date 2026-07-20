# GraphQL - Get Records (Unwrapped Edges) with Shopify

Retrieves records from Shopify from nested GraphQL edges.

## Endpoint

- **Method:** `POST`
- **Path:** `2026-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [GraphQL - Get Records (Unwrapped Edges)](https://shopify.dev/docs/api/admin-graphql/latest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Internal GraphQL query template. |
| `variables` | body | `object` | no | — |
