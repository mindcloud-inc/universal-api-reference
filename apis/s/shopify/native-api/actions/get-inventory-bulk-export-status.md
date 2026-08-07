# Get Inventory Bulk Export Status with Shopify

## Endpoint

- **Method:** `POST`
- **Path:** `2026-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [Get Inventory Bulk Export Status](https://shopify.dev/docs/api/usage/bulk-operations/queries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | — |
| `variables.id` | body | `string` | yes | The bulk operation ID returned by Start Inventory Bulk Export, for example gid://shopify/BulkOperation/720918. |
