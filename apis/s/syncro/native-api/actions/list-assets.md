# List Assets with Syncro

Retrieves a list of assets from Syncro.

## Endpoint

- **Method:** `GET`
- **Path:** `/customer_assets`
- **Base URL:** `https://mindcloud.syncromsp.com/api/v1`
- **Official documentation:** [List Assets](https://api-docs.syncromsp.com/#/Asset/)

## Capabilities

This operation supports [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `snmp_enabled` | query | `boolean` | no | Any assets with SNMP enabled. |
| `customer_id` | query | `number` | no | Any assets attached to a Customer ID. |
| `asset_type_id` | query | `number` | no | Any assets attached to an Asset Type ID. |
| `query` | query | `string` | no | Search query. |
| `page` | query | `number` | no | Returns the provided page of results. |
