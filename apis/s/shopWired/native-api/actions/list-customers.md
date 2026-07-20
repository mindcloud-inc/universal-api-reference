# List customers with ShopWired

Retrieves customers from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [List customers](https://shopwired.readme.io/reference/listcustomers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Search customer records by email address. |
| `trade` | query | `number` | no | 0 for regular customers, 1 for trade customers. |
