# List Virtual Accounts with Finmo

Retrieves virtual accounts from the Finmo platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/virtual-account`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [List Virtual Accounts](https://docs.finmo.net/reference/getallvirtualaccount-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | query | `string` | no | Filter virtual accounts for a specific customer. |
| `include_deleted` | query | `boolean` | no | Include deleted virtual accounts. |
| `created_at` | query | `string` | no | Filter by UTC creation date (YYYY-MM-DD). |
| `start_time` | query | `number` | no | Filter from epoch start timestamp. |
| `end_time` | query | `number` | no | Filter to epoch end timestamp. |
| `limit` | query | `number` | no | Maximum number of records per page. |
| `page` | query | `number` | no | Page number to return. |
