# List Payments with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/payments`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [List Payments](https://api-docs.invoicing.co/#tag/payments/operation/getPayments)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `string` | no | Filter by client. |
| `status` | query | `string` | no | Filter by payment status. |
| `filter` | query | `string` | no | Free-text filter value. |
