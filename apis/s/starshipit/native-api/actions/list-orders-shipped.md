# List Orders (Shipped) with Starshipit

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/shipped`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [List Orders (Shipped)](https://api-docs.starshipit.com/#abbdf631-21c8-472b-b2e7-b1b68b01f6d0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since_last_updated` | query | `date` | no | Show orders recently updated after date in UTC (date-time in RFC3339 format) |
| `ids_only` | query | `boolean` | no | Show all unshipped order_ids |
| `limit` | query | `number` | no | Amount of results (default: 50) (maximum: 250) |
| `page` | query | `number` | no | Page to show (default: 1) |
