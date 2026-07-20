# List Payment Methods with LimoExpress

Retrieves payment methods from the LimoExpress organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/payment-methods`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [List Payment Methods](https://api.limoexpress.me/api/docs/v1#/Payment%20Methods/getAllPaymentMethods)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_string` | query | `string` | no | Search across payment method fields. |
| `page` | query | `number` | no | Page number, default is 1. |
| `per_page` | query | `number` | no | Items per page, default is 20. |
