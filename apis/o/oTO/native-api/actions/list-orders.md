# List Orders with OTO

Retrieves a list of orders from OTO.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.tryoto.com/rest/v2`
- **Official documentation:** [List Orders](https://help.tryoto.com/en/support/solutions/articles/150000213808-orders-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `perPage` | query | `number` | no | Maximum number of orders to return per page. |
| `page` | query | `number` | no | Page number to fetch. |
