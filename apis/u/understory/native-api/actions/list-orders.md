# List Orders with Understory

Retrieves orders from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/orders`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Orders](https://developer.understory.io/apis/order/getorders.md)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | no | Filter orders after this timestamp. |
| `to` | query | `date` | no | Filter orders before this timestamp. |
