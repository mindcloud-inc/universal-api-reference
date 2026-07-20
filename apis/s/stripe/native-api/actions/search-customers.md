# Search Customers with Stripe

Finds customers in Stripe by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `customers/search`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [Search Customers](https://docs.stripe.com/api/customers/search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query string, such as name:'Jane Doe' AND metadata['foo']:'bar'. |
| `limit` | query | `number` | no | Number of customers to return (1-100). |
| `page` | query | `string` | no | Pagination cursor for next page from a prior search response. |
