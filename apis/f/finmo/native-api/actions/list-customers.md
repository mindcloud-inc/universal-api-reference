# List Customers with Finmo

Retrieves customers from the Finmo platform.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer`
- **Base URL:** `https://api.finmo.net/v1/`
- **Official documentation:** [List Customers](https://docs.finmo.net/reference/getallcustomers-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Filter customers by type. |
| `created_at` | query | `string` | no | Filter by UTC creation date (YYYY-MM-DD). |
| `include_deleted` | query | `boolean` | no | Include deleted customers in the results. |
| `start_time` | query | `number` | no | Filter from epoch start timestamp. |
| `end_time` | query | `number` | no | Filter to epoch end timestamp. |
| `limit` | query | `number` | no | Maximum number of records per page. |
| `page` | query | `number` | no | Page number to return. |
