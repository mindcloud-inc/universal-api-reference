# List All Currencies with LimoExpress

Retrieves all currencies from the LimoExpress platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/integration/all-currencies`
- **Base URL:** `https://api.limoexpress.me`
- **Official documentation:** [List All Currencies](https://api.limoexpress.me/api/docs/v1#/Currencies/getAllCurrencies)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_string` | query | `string` | no | Search across currency fields. |
| `page` | query | `number` | no | Page number, default is 1. |
| `per_page` | query | `number` | no | Items per page, default is 20. |
