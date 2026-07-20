# List Orders with SureCart

## Endpoint

- **Method:** `GET`
- **Path:** `v1/orders`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [List Orders](https://developer.surecart.com/api-reference/orders/list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `live_mode` | query | `boolean` | no | Only return live mode or test mode orders. |
| `query` | query | `string` | no | Full-text search query for the order collection. |
