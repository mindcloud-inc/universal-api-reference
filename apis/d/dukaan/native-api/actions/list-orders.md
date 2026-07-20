# List Orders with Dukaan

Retrieves orders from Dukaan.

## Endpoint

- **Method:** `GET`
- **Path:** `api/seller-front/order-list/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [List Orders](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_at_after` | query | `date` | no | Lower bound order creation date. |
| `created_at_before` | query | `date` | no | Upper bound order creation date. |
