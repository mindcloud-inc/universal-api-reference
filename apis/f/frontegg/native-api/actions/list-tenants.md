# List Tenants with Frontegg

Finds accounts in your Frontegg environment.

## Endpoint

- **Method:** `GET`
- **Path:** `/tenants/resources/tenants/v2`
- **Base URL:** `https://api.frontegg.com`
- **Official documentation:** [List Tenants](https://developers.frontegg.com/ciam/api/tenants/accounts)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_limit` | query | `number` | no | Maximum number of tenants to return (default 50, maximum 200). |
| `_offset` | query | `number` | no | Page number to retrieve, starting at 0. |
| `_filter` | query | `string` | no | Filter tenants by name or tenant ID. |
| `_sortBy` | query | `string` | no | Sort by createdAt, name, or tenantId. |
| `_order` | query | `string` | no | Sort order: ASC or DESC. |
| `_tenantIds` | query | `string` | no | Specific tenant IDs to retrieve. |
