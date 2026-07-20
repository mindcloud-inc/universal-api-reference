# List Technologies with PredictLeads

Retrieves tracked technologies from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/technologies`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Technologies](https://docs.predictleads.com/api_endpoints/technologies_dataset/retrieve_all_tracked_technologies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fuzzy_name` | query | `string` | no | Filter results based on the technology fuzzy name. |
| `order_by` | query | `string` | no | Order technologies by created_at_asc, created_at_desc, or fuzzy_score_desc. |
| `page` | query | `number` | no | Page number of shown items. |
| `limit` | query | `number` | no | Limit the number of shown items per page. |
