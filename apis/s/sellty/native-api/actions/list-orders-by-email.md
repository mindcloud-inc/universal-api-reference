# List Orders By Email with Sellty

## Endpoint

- **Method:** `POST`
- **Path:** `/seller/api/v-1-0/get-orders-by-email`
- **Base URL:** `https://my.sellty.ru`
- **Official documentation:** [List Orders By Email](https://my.sellty.ru/seller/docs/api-docs.json)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Customer email address. |
