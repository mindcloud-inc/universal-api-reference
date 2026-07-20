# List Products with PredictLeads

Retrieves products from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/discover/products/latest`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Products](https://docs.predictleads.com/api_endpoints/products_dataset/retrieve_a_list_of_products)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sources` | query | `string` | no | Comma-separated product sources. Supported values: menu, pricing. Send multiple values as a string separated by `,`. |
| `first_seen_at_from` | query | `date` | no | Only return products first seen after the given date (ISO 8601). |
| `first_seen_at_until` | query | `date` | no | Only return products first seen before the given date (ISO 8601). |
| `page` | query | `number` | no | Page number of shown items. |
| `limit` | query | `number` | no | Limit the number of shown items per page. |
