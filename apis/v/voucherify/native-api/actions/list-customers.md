# List Customers with Voucherify

Retrieves a list of customers from Voucherify.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://us1.api.voucherify.io/v1`
- **Official documentation:** [List Customers](https://docs.voucherify.io/reference/list-customers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for paginated customer results. |
| `limit` | query | `number` | no | Maximum number of customers to return. |
