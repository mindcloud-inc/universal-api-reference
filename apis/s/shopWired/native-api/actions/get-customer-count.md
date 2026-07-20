# Get total customer count with ShopWired

Retrieves the total customer count from ShopWired.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/count`
- **Base URL:** `https://api.ecommerceapi.uk/v1`
- **Official documentation:** [Get total customer count](https://shopwired.readme.io/reference/getcustomercount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trade` | query | `number` | yes | 0 for regular customers, 1 for trade customers. |
