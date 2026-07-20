# List Orders (Unshipped) with Starshipit

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/unshipped`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [List Orders (Unshipped)](https://api-docs.starshipit.com/#6dd10a47-8403-4c7e-9b3f-32bf9986d8f3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since_order_date` | query | `date` | no | (optional) Show orders created after date in UTC (date-time in RFC3339 format) |
| `since_last_updated` | query | `date` | no | (optional) Show orders recently updated after date in UTC (date-time in RFC3339 format) |
| `ids_only` | query | `string` | no | (optional) Show all unshipped order_ids only |
| `limit` | query | `string` | no | (optional) Amount of results (default: 50) (maximum: 250) |
| `page` | query | `string` | no | (optional) Page to show (default: 1) |
