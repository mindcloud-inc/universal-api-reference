# List Wallets with Finmo

Retrieves wallets from the Finmo platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/wallet`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [List Wallets](https://docs.finmo.net/reference/getallwallets-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | query | `string` | no | Filter wallets by category. |
| `created_at` | query | `string` | no | Filter by UTC creation date (YYYY-MM-DD). |
| `start_time` | query | `number` | no | Filter from epoch start timestamp. |
| `end_time` | query | `number` | no | Filter to epoch end timestamp. |
| `limit` | query | `number` | no | Maximum number of records per page. |
| `page` | query | `number` | no | Page number to return. |
| `customer_id` | query | `string` | no | Filter wallets for a specific customer. |
