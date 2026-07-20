# Search Orders with Dukaan

Finds orders in Dukaan by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `api/seller-front/order-list/`
- **Base URL:** `https://api.mydukaan.io`
- **Official documentation:** [Search Orders](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Order search text or order number. |
| `created_at_before` | query | `date` | no | Upper bound order creation date. |
