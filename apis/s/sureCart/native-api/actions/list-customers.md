# List Customers with SureCart

## Endpoint

- **Method:** `GET`
- **Path:** `v1/customers`
- **Base URL:** `https://api.surecart.com`
- **Official documentation:** [List Customers](https://developer.surecart.com/api-reference/customers/list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Only return customers with the given email address. |
| `live_mode` | query | `boolean` | no | Only return customers that are live mode or test mode. |
| `query` | query | `string` | no | Full-text search query for the customer collection. |
