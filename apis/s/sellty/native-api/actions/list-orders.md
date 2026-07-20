# List Orders with Sellty

## Endpoint

- **Method:** `POST`
- **Path:** `/seller/api/v-1-0/get-orders`
- **Base URL:** `https://my.sellty.ru`
- **Official documentation:** [List Orders](https://my.sellty.ru/seller/docs/api-docs.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timestamp` | body | `string` | yes | Required by the Sellty API at runtime. Start date/time for returned orders, for example 2022-10-10 or 2022-10-10 10:10:10. |
