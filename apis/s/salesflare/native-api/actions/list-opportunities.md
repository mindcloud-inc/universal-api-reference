# List Opportunities with Salesflare

## Endpoint

- **Method:** `GET`
- **Path:** `opportunities`
- **Base URL:** `https://api.salesflare.com`
- **Official documentation:** [List Opportunities](https://api.salesflare.com/docs#/Opportunities/getOpportunities)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of opportunities to return. |
| `order_by` | query | `string` | no | Sort expression such as creation_date desc. |
| `search` | query | `string` | no | Free-text search across opportunities. |
| `offset` | query | `number` | no | Number of opportunities to skip before returning results. |
