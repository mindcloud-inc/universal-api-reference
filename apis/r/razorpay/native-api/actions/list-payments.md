# List Payments with Razorpay

Retrieves all payment records from Razorpay.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/payments`
- **Base URL:** `https://api.razorpay.com`
- **Official documentation:** [List Payments](https://razorpay.com/docs/api/payments/fetch-all-payments/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `number` | no | Unix timestamp in seconds to fetch payments from. |
| `to` | query | `number` | no | Unix timestamp in seconds to fetch payments up to. |
