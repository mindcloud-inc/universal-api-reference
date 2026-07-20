# List Orders Summary with Starshipit

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/summary`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [List Orders Summary](https://api-docs.starshipit.com/#c1e28347-54b6-4224-bca7-449469790840)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_status` | query | `string` | no | order status to show order summary of. |
| `sort` | query | `string` | no | Order field to sort by. |
| `sort_direction` | query | `string` | no | sort direction. |
| `filter` | query | `string` | no | Filter the orders returned in the order summary by various filters. This parameter is specified in the following format: Multiple filters can be specified, please seperate these by comma ','. See the Filters section below for accepted filter values. |
| `page` | query | `string` | no | page number. |
| `page_size` | query | `string` | no | number of results to return (default: 500, maximum: 500) |
