# Search Orders with Starshipit

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/search`
- **Base URL:** `https://api.starshipit.com/api`
- **Official documentation:** [Search Orders](https://api-docs.starshipit.com/#7615c4c5-893b-4085-aa67-5d1d34297654)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Amount of results (default: 50) (maximum: 250) |
| `page` | query | `string` | no | Page to show (default: 1) |
| `status` | query | `string` | no | Returns a list of orders based on the order status (default: All) |
| `fields` | query | `string` | no | In. conjunction with the phrase parameter, which field to search. If "All", it will search 'order number', 'tracking number', 'theirRef' and 'name' |
| `include_child_accounts` | query | `string` | no | If set to true, orders from child accounts will be returned (default: false) |
| `phrase` | query | `string` | no | — |
