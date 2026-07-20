# List Customers with Stripe

Retrieves customers from your Stripe account.

## Endpoint

- **Method:** `GET`
- **Path:** `customers`
- **Base URL:** `https://api.stripe.com/v1`
- **Official documentation:** [List Customers](https://docs.stripe.com/api/customers/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Case-sensitive customer email filter. |
| `created` | query | `object` | no | Date interval object for customer creation timestamp filters. |
| `created.gt` | query | `number` | no | Minimum creation timestamp (exclusive). |
| `created.gte` | query | `number` | no | Minimum creation timestamp (inclusive). |
| `created.lt` | query | `number` | no | Maximum creation timestamp (exclusive). |
| `created.lte` | query | `number` | no | Maximum creation timestamp (inclusive). |
| `limit` | query | `number` | no | Number of customers to return (1-100). |
| `starting_after` | query | `string` | no | Pagination cursor for next page. |
| `ending_before` | query | `string` | no | Pagination cursor for previous page. |
| `test_clock` | query | `string` | no | Filter to customers attached to a test clock. |
